<template>
    <footer class="footer">
        <div class="footer-content">
            <nav class="footer-menu">
                <ul class="footer-menu-column">
                    <li class="footer-menu__title">General</li>
                    <li class="footer-menu-elem" @click="sendComponent('Main')">
                        <p class="footer-menu-elem__title">Main</p>
                    </li>
                    <li class="footer-menu-elem" @click="sendComponent('About')">
                        <p class="footer-menu-elem__title">About</p>
                    </li>
                    <li class="footer-menu-elem" @click="sendComponent('Advantages')">
                        <p class="footer-menu-elem__title">Advantages</p>
                    </li>
                    <li class="footer-menu-elem" @click="sendComponent('Contacts')">
                        <p class="footer-menu-elem__title">Contacts</p>
                    </li>
                </ul>
                <ul class="footer-menu-column">
                    <li class="footer-menu__title">Shop</li>
                    <li class="footer-menu-elem">
                        <p class="footer-menu-elem__title">Delivery</p>
                    </li>
                    <li class="footer-menu-elem">
                        <p class="footer-menu-elem__title">Order Status</p>
                    </li>
                    <li class="footer-menu-elem">
                        <p class="footer-menu-elem__title">Shopping Help</p>
                    </li>
                    <li class="footer-menu-elem">
                        <p class="footer-menu-elem__title">Business</p>
                    </li>
                </ul>
            </nav>
            <div class="footer-social">
                <p class="footer-social__title">Social media</p>
                <div class="footer-social__icons">
                    <img class="footer-social__img" src="../assets/facebook.png">
                    <img class="footer-social__img" src="../assets/instagram.png">
                    <img class="footer-social__img" src="../assets/twitter.png">
                    <img class="footer-social__img" src="../assets/youtube.png">
                </div>
            </div>
        </div>
        <p class="footer-rights"> Copyright © 2020 Rick and Morty Ink. All rights reserved.</p>
    </footer>
</template>

<script>
    export default {
        name: "Footer",
        methods: {
            sendComponent(name) {
                this.$emit('changePage', name);
            }
        }
    }
</script>

<style scoped>
    .footer {
        background-color: #2d2d2d;
        bottom: 0;
        left: 0;
        width: 100%;
        margin-top: 130px;
    }
    .footer-content {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        justify-content: space-around;
        padding-top: 25px;
        max-width: 980px;
        margin: 0 auto;
        flex-wrap: wrap;
    }
    .footer-menu {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        flex-wrap: wrap;
        margin-left: 45px;
    }
    .footer-menu-column {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin: 0 0 10px 0;
        padding: 0 40px 0 0;
        list-style: none;
    }
    .footer-menu__title {
        font-size: 16px;
        color: #b2b2b2;
        font-weight: bold;
        cursor: pointer;
        margin: 0 0 3px 0;
    }
    .footer-menu-elem {
        font-size: 12px;
        color: #b2b2b2;
        cursor: pointer;
        margin: 3px 0;

    }
    .footer-menu-elem:hover {
        color: #d0d0d0;
    }
    .footer-menu-elem:first-child {
        margin-top: 0;
    }
    .footer-menu-elem:last-child {
        margin-bottom: 0;
    }
    .footer-menu-elem__title {
        margin: 0;
    }
    .footer-social {
        display: flex;
        flex-direction: column;
        justify-items: flex-start;
    }
    .footer-social__title {
        font-size: 18px;
        color: #b2b2b2;
        margin: 0 0 12px 0;
    }
    .footer-social__icons {
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        cursor: pointer;
    }
    .footer-social__icons:hover {
        color: #d0d0d0;
    }
    .footer-social__img {
        height: 30px;
        margin: 0 10px;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .footer-social__img:first-child {
        margin-left: 0;
    }
    .footer-social__img:last-child {
        margin-right: 0;
    }
    .footer-social__img:hover {
        transform: scale(1.15);
    }
    .footer-rights {
        font-size: 12px;
        text-align: center;
        color: #b2b2b2;
        margin: 0;
        padding: 20px 0 15px;
    }
</style>
