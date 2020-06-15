<template>
    <div class="menu">
        <ul class="menu-box">
            <li>
                <img class="menu-img" src="../assets/menu.png" @click="openMenu">
                <ul class="menu-content" v-if="isOpen">
                    <li class="menu-elem" @click="changePage('Main')">
                        <p class="menu-elem__title">Main</p>
                    </li>
                    <li class="menu-elem" @click="changePage('About')">
                        <p class="menu-elem__title">About</p>
                    </li>
                    <li class="menu-elem" @click="changePage('Advantages')">
                        <p class="menu-elem__title">Advantages</p>
                    </li>
                    <li class="menu-elem" @click="changePage('Contacts')">
                        <p class="menu-elem__title">Contacts</p>
                    </li>
                </ul>
            </li>
        </ul>
        <!--<nav class="menu-box" v-if="isOpen">-->
            <!--<ul class="menu-content">-->
                <!--<li class="menu-elem" @click="changePage('Main')">-->
                    <!--<p class="menu-elem__title">Main</p>-->
                <!--</li>-->
                <!--&lt;!&ndash;<li class="menu-elem" @click="changePage('About')">&ndash;&gt;-->
                    <!--&lt;!&ndash;<p class="menu-elem__title">About</p>&ndash;&gt;-->
                <!--&lt;!&ndash;</li>&ndash;&gt;-->
                <!--&lt;!&ndash;<li class="menu-elem" @click="changePage('Advantages')">&ndash;&gt;-->
                    <!--&lt;!&ndash;<p class="menu-elem__title">Advantages</p>&ndash;&gt;-->
                <!--&lt;!&ndash;</li>&ndash;&gt;-->
                <!--&lt;!&ndash;<li class="menu-elem" @click="changePage('Contacts')">&ndash;&gt;-->
                    <!--&lt;!&ndash;<p class="menu-elem__title">Contacts</p>&ndash;&gt;-->
                <!--&lt;!&ndash;</li>&ndash;&gt;-->
            <!--</ul>-->

            <!--<ul>-->
                <!--<li><a href="/">Главная</a></li>-->
                <!--<li><a href="#">О блоге</a>-->
                    <!--<ul>-->
                        <!--<li><a href="/about">Об авторе</a></li>-->
                        <!--<li><a href="/history">История блога</a></li>-->
                        <!--<li><a href="/privacy-policy">Политика конфиденциальности</a></li>-->
                        <!--<li><a href="/disclaimer">Отказ от ответственности</a></li>-->
                    <!--</ul>-->
                <!--</li>-->
                <!--<li><a href="/sitemap">Карта сайта</a></li>-->
                <!--<li><a href="/contact">Обратная связь</a></li>-->
            <!--</ul>-->
        <!--</nav>-->
    </div>
</template>

<script>
    export default {
        name: "BurgerMenu",
        data() {
          return {
              isOpen: false
          }
        },
        methods: {
            changePage(name) {
                this.$emit('changePage', name);
                this.isOpen = false;
            },
            openMenu() {
                this.isOpen = !this.isOpen;
            }
        }
    }
</script>

<style scoped>
    .menu {
        display: flex;
        align-items: center;
        margin: 0 10px 0 0;
    }
    .menu-box {
        list-style: none;
        padding: 0;
    }
    .menu-img {
        max-height: 25px;
        cursor: pointer;
        padding-left: 30px;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .menu-img:hover {
        transform: scale(1.05);
    }
    .menu-content {
        background-color: #2d2d2d;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        padding: 30px 60px 10px 30px;
        margin: 0 0 0 0;
        list-style: none;
        position: absolute;
        /*visibility: hidden;*/
    }
    .menu-elem {
        font-size: 18px;
        color: #b2b2b2;
        cursor: pointer;
        padding: 15px 0 15px 0;
    }
    .menu-elem:hover {
        color: #d0d0d0;
    }
    .menu-elem:first-child {
        margin-top: 0;
    }
    .menu-elem:last-child {
        margin-bottom: 0;
    }
    .menu-elem__title {
        margin: 0;
    }
</style>
