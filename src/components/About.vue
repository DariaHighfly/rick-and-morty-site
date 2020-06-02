<template>
    <div class="about">
        <p class="about__title">About Us</p>
        <hr class="about__line"/>
        <p class="about__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Asperiores at commodi error est exercitationem fugit,
            hic illo illum ipsum iure iusto labore modi pariatur quasi quibusdam
            repellendus sapiente suscipit tempore?</p>
        <div class="about-content">
            <div class="about-content-card">
                <div class="about-content-card__border">
                    <img class="about-content-card__img custom-first" src="../assets/about-rick.jpg"/>
                    <p class="about-content-card__text">-Rick</p>
                </div>
            </div>
            <div class="about-content-card">
                <div class="about-content-card__border">
                    <img class="about-content-card__img custom-second" src="../assets/about-morty.jpg"/>
                    <p class="about-content-card__text">-Morty</p>
                </div>
            </div>
            <div class="about-content-card">
                <div class="about-content-card__border">
                    <img class="about-content-card__img custom-third" src="../assets/about-you.png"/>
                    <p class="about-content-card__text">-You</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "About"
    }
</script>

<style scoped>
    .about {
        display: flex;
        flex-direction: column;
        justify-items: center;
        align-items: center;
        max-width: 980px;
        margin: 0 auto;
        padding: 100px 0 50px 0;
    }
    .about__title {
        font-size: 28px;
        font-weight: bold;
        margin: 10px 0;
    }
    .about__line {
        height: 2px;
        width: 70px;
        background-color: black;
        border: none;
        margin: 10px 0 10px 0;
    }
    .about__text {
        font-size: 18px;
        text-align: center;
        margin: 20px 0 40px 0;
        max-width: 70%;
    }
    .about-content {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }
    .about-content-card {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: #FFFFFF;
        margin: 20px 20px 0 0;
        padding: 21px 17px 26px 17px;
        border-radius: 4px;
        -webkit-box-shadow: 6px 7px 13px 2px rgba(0,0,0,0.11);
        -moz-box-shadow: 6px 7px 13px 2px rgba(0,0,0,0.11);
        box-shadow: 6px 7px 13px 2px rgba(0,0,0,0.11);
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .about-content-card:hover {
        transform: scale(1.05);
    }
    .about-content-card__border {
        border: 2px solid #000000;
        border-radius: 3px;
        margin: 5px;
        padding: 5px;
    }
    .about-content-card__img {
        height: 280px;
        width: 122px;
        margin: 20px 60px 10px 60px;
    }
    .custom-first {
    }
    .custom-second {
        height: 260px;
        width: 120px;
        margin: 45px 61px 15px 61px;
    }
    .custom-third {
        height: 240px;
        width: 118px;
        margin: 45px 62px 35px 62px;
    }
    .about-content-card__text {
        font-family: 'Permanent Marker', sans-serif;
        font-size: 22px;
        text-align: right;
        margin: 0 15px 0 0;
    }
</style>
