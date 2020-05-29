<template>
    <div class="search">
        <img src=../assets/search.png class="search__img">
    </div>
</template>

<script>
    export default {
        name: "Search"
    }
</script>

<style scoped>
    .search {
        display: flex;
        align-items: center;
        margin: 0 10px 0 0;
    }
    .search__img {
        max-height: 25px;
    }
</style>
