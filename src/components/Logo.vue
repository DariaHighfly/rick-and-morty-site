<template>
    <div class="logo">
        <img src=../assets/logo.png class="logo__img">
    </div>
</template>

<script>
    export default {
        name: "Logo"
    }
</script>

<style scoped>
    .logo {
        display: flex;
        align-items: center;
        margin: 8px 10px 8px 0;
    }
    .logo__img {
        max-height: 50px;
        cursor: pointer;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .logo__img {
        transform: scale(1.05);
    }
</style>
