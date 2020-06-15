<template>
    <div class="contacts">
        <p class="contacts__title">Contacts</p>
        <hr class="contacts__line"/>
        <div class="contacts-content">
            <div class="contacts-content-column">
                <div class="contacts-content-column__row">
                    <img class="contacts-content__pic" src="../assets/pin.png">
                    <p class="contacts-content-column__title">Address</p>
                </div>
                <p class="contacts-content-column__text"> 700 E 9th St <br/> New York  <br/> NY 10009, USA</p>
            </div>
            <div class="contacts-content-column">
                <div class="contacts-content-column__border">
                    <img class="contacts-content-column__map" src="../assets/map.jpg">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Contacts"
    }
</script>

<style scoped>
    .contacts {
        display: flex;
        flex-direction: column;
        justify-items: center;
        align-items: center;
        max-width: 980px;
        margin: 0 auto;
        padding: 100px 0 50px 0;
    }
    .contacts__title {
        font-size: 28px;
        font-weight: bold;
        margin: 10px 0;
    }
    .contacts__line {
        height: 2px;
        width: 70px;
        background-color: black;
        border: none;
        margin: 10px 0 10px 0;
    }
    .contacts-content {
        justify-content: center;
        align-items: flex-start;
        margin: 30px 0 30px 0;
    }
    .contacts-content__pic {
        height: 40px;
        margin: 0 10px 0 0;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .contacts-content__pic:hover {
        transform: scale(1.05);
    }
    .contacts-content-column {
        margin-right: 160px;
    }
    .contacts-content-column:last-child {
        margin-right: 0;
    }
    .contacts-content-column__row {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: flex-start;
    }
    .contacts-content-column__title {
        font-size: 18px;
        font-weight: bold;
        margin: 20px 0 10px 0;
    }
    .contacts-content-column__text {
        font-size: 14px;
        margin-left: 10px;
    }
    .contacts-content-column__border {
        border: 2px solid #000000;
        border-radius: 3px;
        margin: 5px;
        padding: 10px;
    }
    .contacts-content-column__map {
        height: auto;
        width: 50vh;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .contacts-content-column__map:hover {
        transform: scale(1.02);
    }
    @media screen and (min-width: 980px) {
        .contacts-content {
            display: flex;
            flex-direction: row;
        }
    }
    @media screen and (max-width: 980px) {
        .contacts-content {
            display: flex;
            flex-direction: column;
        }
    }
</style>
