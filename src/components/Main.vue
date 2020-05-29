<template>
    <div class="main">
        <div class="main-content" :class="{
             'main-content__pic' : (videoFlag && (windowTop < videoBegins))}">
            <div class="main-text">
                <p class="main-text__header">Wuba<br/>luba<br/>dub-dub!</p>
            </div>
            <!--autoplay loop-->
            <video autoplay muted :class="{
             'main-video__hide' : (videoFlag && (windowTop < videoBegins)),
             'main-video' : (!videoFlag || windowTop >= videoBegins)}">
                <source src="../assets/RM.mp4" type="video/mp4">
                Your browser does not support HTML5 video.
            </video>
        </div>
        <div class="video-back">
        </div>
    </div>
</template>

<script>
    export default {
        name: "Main",
        data(){
            return {
                windowTop: 0,
                videoFlag: 1,
                videoBegins: 535,
            };
        },
        mounted()
        {
            let that = this;
            window.addEventListener("scroll", function() {
                that.windowTop = window.scrollY;
                if (that.videoFlag === 1 && window.scrollY > that.videoBegins) {
                    that.videoFlag = 0;
                }
            });
        },
    }
</script>

<style scoped>
    .main {
        background-color: #ffffff;
        padding-top: 35px;
    }
    .main-content {
        background-color: #ffffff;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        max-width: 980px;
        margin: 0 auto;
        /*padding-top: 0px;*/
        min-height: 1240px;
    }
    .main-content__pic {
        background-image: url(../assets/main_background.png);
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: 82%;
    }
    .main-text {
        /*position: fixed;*/
        /*bottom: 0;*/
        margin: 170px 0 0 70px;
    }
    .main-text__header {
        font-family: 'Bebas Neue', sans-serif;
        font-size: 170px;
        color: #1d1d1d;
        text-transform: uppercase;
        line-height: 0.8em;
        margin: 0;
    }
    .main-video {
        /*position: fixed;*/
        /*right: 0;*/
        /*bottom: 0;*/
        /*top: 110px;*/
        width: 120%;
        align-items: center;
        margin: 0 -98px;
        /*display: none;*/
    }
    .main-video__hide {
        display: none;
    }
    .video-back {
        height: 800px;
    }
</style>
