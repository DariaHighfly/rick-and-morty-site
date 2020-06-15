<template>
    <div class="main">
        <div class="main-content">
            <div class="main-text">
                <p class="main-text__header">Wuba<br/>luba<br/>dub-dub!</p>
            </div>
            <div class="gap"></div>
            <!--autoplay loop-->
            <!--:current-time.prop="currentTime"-->
            <!--@timeupdate="currentTime = $event.target.currentTime"-->
            <video muted
                   id="video"
                   :class="{
                   'main-video' : (videoFixedFlag && (windowTop < videoStops)),
                   'fixed' : (!videoFixedFlag || (windowTop >= videoStops))}">
                <source src="../assets/RM.mp4" type="video/mp4">
                Your browser does not support HTML5 video.
            </video>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Main",
        data(){
            return {
                windowTop: 0,
                videoBegins: 310,
                videoStops: 660,
                videoFixedFlag: 1,
                videoPlay: 0,
                // currentTime: 0,
            };
        },
        mounted()
        {
            let that = this;
            window.addEventListener("scroll", function() {
                that.windowTop = window.scrollY;
                if (that.videoPlay === 0 && window.scrollY > that.videoBegins) {
                    that.videoPlay = 1;
                }
                if (that.videoFixedFlag === 1 && window.scrollY > that.videoStops) {
                    that.videoFixedFlag = 0;
                }
                // if (window.scrollY > that.videoBegins && window.scrollY < that.videoStops) {
                //     if (window.scrollY < 560) {
                //         that.currentTime = (window.scrollY - that.videoBegins) * 0.007;
                //     } else {
                //         that.currentTime = (window.scrollY - that.videoBegins) * 0.02;
                //     }
                // }
            });
        },
        watch: {
            videoPlay(val) {
                let videoElem = document.getElementById("video");
                videoElem.play();
            }
        }
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
        padding-top: 35px;
    }
    .main-text {
        z-index: 1;
    }
    .main-text__header {
        font-family: 'Bebas Neue', sans-serif;
        /*font-size: 175px;*/
        font-size: 21vh;
        color: #1d1d1d;
        text-transform: uppercase;
        line-height: 0.8em;
        margin: 0;
    }
    .gap {
        height: 100px;
    }
    @media screen and (min-width: 980px) {
        .main-content {
            min-height: 1180px;
        }
        .main-text {
            z-index: 1;
            margin: 150px 0 0 70px;
        }
        .main-video {
            position: fixed;
            top: 10%;
            max-width: 980px;
        }
        .fixed {
            position: inherit;
            max-width: 980px;
        }
    }
    @media screen and (max-width: 980px) {
        .main-text {
            z-index: 1;
            margin: 100px 0 0 70px;
        }
        .main-video {
            display: none;
        }
        .fixed {
            display: none;
        }
    }
    .video-back {
        height: 800px;
    }
</style>
