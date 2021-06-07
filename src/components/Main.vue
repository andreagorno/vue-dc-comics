<template>
    <div class="main">
        <div class="content">
            <div class="container">
                <span>Content goes here</span>
            </div>
        </div>
        <div class="info">
            <div class="container">
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <img :src="link.url" :alt="link.alt">
                        <span>{{ link.name }}</span>
                    </li>
                    
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Main",

    data: function() {
        return {
            links: [
                {
                    name: "digital comics",
                    url: require("../assets/buy-comics-digital-comics.png"),
                    alt: "digital-comics"
                },
                {
                    name: "dc merchandise",
                    url: require("../assets/buy-comics-merchandise.png"),
                    alt: "dc-merchandise"
                },
                {
                    name: "subscriptions",
                    url: require("../assets/buy-comics-subscriptions.png"),
                    alt: "subscriptions"
                },
                {
                    name: "comic shop locator",
                    url: require("../assets/buy-comics-shop-locator.png"),
                    alt: "comic-shop-locator"
                },
                {
                    name: "dc power visa",
                    url: require("../assets/buy-dc-power-visa.svg"),
                    alt: "dc-power-visa"
                }
            ],
        }
    }
}
</script>

<style scoped lang="scss">
    @import "../style/variables";

    .content {
        background-color: rgba($color: #000000, $alpha: 0.9);

        div {
            display: flex;
            align-items: center;
            height: 125px;

            span {
                font-size: 26px;
                color: white;
            }
        }
    }

    .info {
        background-color: $brandColor;

        .container {
            display: flex;
            height: 125px;
            
            
            ul {
                list-style: none;
                display: flex;
                align-items: center;
                flex-grow: 1;
                

                li {
                    display: flex;
                    align-items: center;
                    margin: 0 10px;
                    flex-grow: 1;
                    

                    img {
                        height: 40px;
                        margin-right: 10px;
                    }

                    span {
                        font-size: 14px;
                        color: white;
                        text-transform: uppercase;
                    }
                }
            }
        }
    }
</style>