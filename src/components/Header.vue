<template>
    <header class="header">
        <nav class="header-content">
            <div class="header-content__desktop">
                <Logo></Logo>
                <Menu @changePage="sendComponent"></Menu>
                <Search></Search>
            </div>
            <div class="header-content__mobile">
                <BurgerMenu @changePage="sendComponent"></BurgerMenu>
                <Logo></Logo>
                <Search></Search>
            </div>
        </nav>
    </header>
</template>

<script>
    import Logo from "./Logo"
    import Menu from "./Menu"
    import BurgerMenu from "./BurgerMenu"
    import Search from "./Search"

    export default {
        name: "Header",
        components: {
            Logo,
            Menu,
            BurgerMenu,
            Search
        },
        methods: {
            sendComponent(name) {
                this.$emit('changePage', name);
            }
        }
    }
</script>

<style scoped>
    .header {
        position: fixed;
        z-index: 10;
        background-color: #2d2d2d;
        top: 0;
        left: 0;
        width: 100%;
    }
    .header-content__desktop, .header-content__mobile {
        display: flex;
        align-items: center;
        background-color: #2d2d2d;
        max-width: 980px;
        margin: 0 auto;
    }
    .header-content__desktop {
        justify-content: space-around;
    }
    .header-content__mobile {
        justify-content: space-between;
    }
    @media screen and (min-width: 980px) {
        .header-content__mobile {
            display: none;
        }
    }
    @media screen and (max-width: 980px) {
        .header-content__desktop {
            display: none;
        }
    }
</style>
