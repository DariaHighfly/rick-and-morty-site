<template>

</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>

</style>

<!--<template>-->
    <!--<div class="main">-->
        <!--<div class="main-content" id="content">-->
            <!--<div class="main-text">-->
                <!--<p class="main-text__header">Wuba<br/>luba<br/>dub-dub!</p>-->
            <!--</div>-->
            <!--&lt;!&ndash;autoplay loop&ndash;&gt;-->
            <!--<video muted tabindex="4" id="video" class="main-video">-->
                <!--<source src="../assets/RM.mp4" type="video/mp4">-->
                <!--Your browser does not support HTML5 video.-->
            <!--</video>-->
        <!--</div>-->
        <!--&lt;!&ndash;<div class="main-content" id="content" :class="{&ndash;&gt;-->
        <!--&lt;!&ndash;'main-content__pic' : (windowTop < videoBegins)}">&ndash;&gt;-->
        <!--&lt;!&ndash;<div class="main-text">&ndash;&gt;-->
        <!--&lt;!&ndash;<p class="main-text__header">Wuba<br/>luba<br/>dub-dub! {{windowTop}}</p>&ndash;&gt;-->
        <!--&lt;!&ndash;</div>&ndash;&gt;-->
        <!--&lt;!&ndash;&lt;!&ndash;autoplay loop&ndash;&gt;&ndash;&gt;-->
        <!--&lt;!&ndash;<video muted tabindex="4" id="video" :class="{&ndash;&gt;-->
        <!--&lt;!&ndash;'main-video__hide' : (windowTop < videoBegins), 'main-video' : (windowTop >= videoBegins)}">&ndash;&gt;-->
        <!--&lt;!&ndash;<source src="../assets/RM.mp4" type="video/mp4">&ndash;&gt;-->
        <!--&lt;!&ndash;Your browser does not support HTML5 video.&ndash;&gt;-->
        <!--&lt;!&ndash;</video>&ndash;&gt;-->
        <!--&lt;!&ndash;</div>&ndash;&gt;-->
        <!--<div class="video-back">-->
        <!--</div>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
        <!--<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.-->
            <!--Consequuntur facere inventore quae qui voluptatibus. Accusantium,-->
            <!--animi consequatur corporis cum dignissimos itaque laudantium minus necessitatibus-->
            <!--officia officiis omnis, porro possimus saepe.</p>-->
    <!--</div>-->
<!--</template>-->

<!--<script>-->
    <!--export default {-->
        <!--name: "Main",-->
        <!--data(){-->
            <!--return {-->
                <!--windowTop: 0,-->
                <!--videoBegins: 500,-->
                <!--frameNumber: 0,-->
                <!--playbackConst: 500,-->
            <!--};-->
        <!--},-->
        <!--mounted()-->
        <!--{-->
            <!--let that = this;-->
            <!--window.addEventListener("scroll", function(){-->
                <!--that.windowTop = window.scrollY;-->
            <!--});-->
            <!--this.frameNumber = 0; // start video at frame 0-->
            <!--// lower numbers = faster playback-->
            <!--// get page height from video duration-->
            <!--let setHeight = document.getElementById("content");-->
            <!--// select video element-->
            <!--let vid = document.getElementById('video');-->
            <!--// var vid = $('#v0')[0]; // jquery option-->

            <!--// dynamically set the page height according to video length-->
            <!--vid.addEventListener('loadedmetadata', function() {-->
                <!--setHeight.style.height = Math.floor(vid.duration) * this.playbackConst + "px";-->
            <!--});-->
            <!--// Use requestAnimationFrame for smooth playback-->
            <!--function scrollPlay(){-->
                <!--this.frameNumber  = window.pageYOffset/this.playbackConst;-->
                <!--vid.currentTime  = this.frameNumber;-->
                <!--window.requestAnimationFrame(scrollPlay);-->
            <!--}-->

            <!--window.requestAnimationFrame(scrollPlay);-->
        <!--},-->
    <!--}-->
<!--</script>-->

<!--<style scoped>-->
    <!--.main {-->
        <!--background-color: #ffffff;-->
    <!--}-->
    <!--.main-content {-->
        <!--background: none;-->
        <!--display: flex;-->
        <!--flex-direction: column;-->
        <!--justify-content: flex-start;-->
        <!--max-width: 980px;-->
        <!--margin: 0 auto;-->
        <!--/*padding-top: 0px;*/-->
        <!--min-height: 1240px;-->
    <!--}-->
    <!--/*.main-content__pic {*/-->
    <!--/*background-image: url(../assets/main_background.png);*/-->
    <!--/*background-attachment: fixed;*/-->
    <!--/*background-position: center;*/-->
    <!--/*background-repeat: no-repeat;*/-->
    <!--/*background-size: 82%;*/-->
    <!--/*}*/-->
    <!--.main-text {-->
        <!--position: fixed;-->
        <!--bottom: 0;-->
        <!--z-index: 2;-->
        <!--margin: 170px 0 0 70px;-->
    <!--}-->
    <!--.main-text__header {-->
        <!--font-family: 'Bebas Neue', sans-serif;-->
        <!--font-size: 170px;-->
        <!--color: #1d1d1d;-->
        <!--text-transform: uppercase;-->
        <!--line-height: 0.8em;-->
        <!--margin: 0;-->
    <!--}-->
    <!--.main-video {-->
        <!--position: fixed;-->
        <!--right: 0;-->
        <!--bottom: 0;-->
        <!--width: 100%;-->
        <!--align-items: center;-->
        <!--margin: 0 -100px;-->
        <!--z-index: -1;-->
        <!--/*display: none;*/-->
    <!--}-->
    <!--.main-video__hide {-->
        <!--display: none;-->
    <!--}-->
    <!--.video-back {-->
        <!--height: 800px;-->
    <!--}-->
<!--</style>-->
