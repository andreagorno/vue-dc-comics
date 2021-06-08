<template>
    <div class="card">
        <img :src="img">
        <h3> {{ Title }} </h3>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: {
        img: String,
        Title: String
    }
}
</script>

<style lang="scss">
    .card {
        width: calc(100% / 6);
        padding: 10px;
        img {
            display: inline-block;
            width: 100%;
        }
    }
    h3 {
        color: white;
        display: inline-block;
    }
</style>