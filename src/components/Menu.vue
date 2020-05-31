<template>
    <div class="menu">
        <ul class="menu-content">
            <li class="menu-elem">
                <p class="menu-elem__title">Main</p>
            </li>
            <li class="menu-elem">
                <p class="menu-elem__title">About</p>
            </li>
            <li class="menu-elem">
                <p class="menu-elem__title">Advantages</p>
            </li>
            <li class="menu-elem">
                <p class="menu-elem__title">Contacts</p>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "Menu"
    }
</script>

<style scoped>
    .menu {
        display: flex;
        align-items: center;
        margin: 0 10px 0 0;
    }
    .menu-content {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        padding: 0 5px;
        margin: 0;
        list-style: none;
    }
    .menu-elem {
        font-size: 16px;
        color: #b2b2b2;
        cursor: pointer;
        margin: 0 30px;
    }
    .menu-elem:hover {
        color: #d0d0d0;
    }
    .menu-elem:first-child {
        margin-left: 0;
    }
    .menu-elem:last-child {
        margin-right: 0;
    }
    .menu-elem__title {
        margin: 0;
    }
</style>
