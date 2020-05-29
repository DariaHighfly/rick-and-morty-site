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
    }
</style>
