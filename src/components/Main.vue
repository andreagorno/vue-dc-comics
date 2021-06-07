<template>
    <div class="main">
        <div class="content">
            <div>
                <span>Content goes here</span>
            </div>
        </div>
        <div class="info">
            <div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Main",
}
</script>

<style scoped lang="scss">
    .content {
        background-color: rgba($color: #000000, $alpha: 0.9);

        div {
            display: flex;
            align-items: center;
            width: 80%;
            height: 125px;
            margin: auto;

            span {
                font-size: 26px;
                color: white;
            }
        }
    }

    .info {
        background-color: #0282F9;

        div {
            display: flex;
            align-items: center;
            width: 80%;
            height: 125px;
            margin: auto;
        }
    }
</style>