<template>
    <header class="header">
        <nav class="header-content">
            <Logo></Logo>
            <Menu></Menu>
            <Search></Search>
        </nav>
    </header>
</template>

<script>
    import Logo from "./Logo"
    import Menu from "./Menu"
    import Search from "./Search"

    export default {
        name: "Header",
        components: {
            Logo,
            Menu,
            Search
        },
    }
</script>

<style scoped>
    .header {
        position: fixed;
        background-color: #2d2d2d;
        top: 0;
        left: 0;
        width: 100%;
    }
    .header-content {
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-color: #2d2d2d;
        max-width: 980px;
        margin: 0 auto;
    }
</style>
