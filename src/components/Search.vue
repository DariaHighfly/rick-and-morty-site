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
        margin: 0 30px 0 0;
    }
    .search__img {
        max-height: 25px;
        cursor: pointer;
        transform: scale(1);
        transition: 0.2s all ease;
    }
    .search__img:hover {
        transform: scale(1.05);
    }
</style>
