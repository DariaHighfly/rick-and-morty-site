<template>
    <div class="advantages">
        <p class="advantages__title">Advantages</p>
        <hr class="advantages__line"/>
        <div class="advantages-content">
            <div class="advantages-content-elem">
                <div class="advantages-content-elem__border">
                    <img class="advantages-content-elem__img" src="../assets/logo.png">
                </div>
                <p class="advantages-content-elem__title">Rick</p>
                <p class="advantages-content-elem__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Ab cumque delectus eius impedit incidunt ipsum, molestiae mollitia officia pariatur quia repudiandae
                    sequi sint ullam voluptas voluptatem!</p>
            </div>
            <div class="advantages-content-elem">
                <div class="advantages-content-elem__border">
                    <img class="advantages-content-elem__img" src="../assets/logo.png">
                </div>
                <p class="advantages-content-elem__title">Rick</p>
                <p class="advantages-content-elem__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Ab cumque delectus eius impedit incidunt ipsum, molestiae mollitia officia pariatur quia repudiandae
                    sequi sint ullam voluptas voluptatem!</p>
            </div>
            <div class="advantages-content-elem">
                <div class="advantages-content-elem__border">
                    <img class="advantages-content-elem__img" src="../assets/logo.png">
                </div>
                <p class="advantages-content-elem__title">Rick</p>
                <p class="advantages-content-elem__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Ab cumque delectus eius impedit incidunt ipsum, molestiae mollitia officia pariatur quia repudiandae
                    sequi sint ullam voluptas voluptatem!</p>
            </div>
            <div class="advantages-content-elem">
                <div class="advantages-content-elem__border">
                    <img class="advantages-content-elem__img" src="../assets/logo.png">
                </div>
                <p class="advantages-content-elem__title">Rick</p>
                <p class="advantages-content-elem__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Ab cumque delectus eius impedit incidunt ipsum, molestiae mollitia officia pariatur quia repudiandae
                    sequi sint ullam voluptas voluptatem!</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Advantages"
    }
</script>

<style scoped>
    .advantages {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 980px;
        margin: 0 auto;
        padding: 100px 0 50px 0;
    }
    .advantages__title {
        font-size: 28px;
        font-weight: bold;
        margin: 10px 0;
    }
    .advantages__line {
        height: 2px;
        width: 70px;
        background-color: black;
        border: none;
        margin: 10px 0 20px 0;
    }
    .advantages-content {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        margin: 30px 0;
        flex-wrap: wrap;
    }
    .advantages-content-elem {
        display: flex;
        flex-direction: column;
        justify-items: center;
        align-items: center;
        margin-right: 35px;
        max-width: 200px;
    }
    .advantages-content-elem:last-child {
        margin-right: 0;
    }
    .advantages-content-elem__border {
        border: 2px solid #000000;
        border-radius: 100%;
        padding: 30px;
    }
    .advantages-content-elem__img {
        height: 105px;
        width: auto;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .advantages-content-elem__img:hover {
        transform: scale(1.15);
    }
    .advantages-content-elem__title {
        font-size: 20px;
        font-weight: bold;
        text-align: center;
        margin: 10px 0;
    }
    .advantages-content-elem__text {
        font-size: 14px;
        text-align: center;
        width: inherit;
        max-width: 95%;
    }
</style>
