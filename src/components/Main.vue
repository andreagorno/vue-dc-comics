<template>
    <div class="main">
        <div class="content">
            <div class="container container-comics">
                <Card 
                v-for="(comic, index) in comics" 
                :key="index"
                :img="comic.thumb"
                :Title="comic.series" />
            </div>
            <div class="container align-center">
                <button class="blue-button">load more</button>
                <button class="blue-button absolute">current series</button>
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
import Card from './Card';

export default {
    name: "Main",

    components: {
        Card
    },

    data: function() {
        return {
            comics: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/ Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/ Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ],

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
        position: relative;

        .container-comics {
            display: flex;
            flex: row;
            justify-content: left;
            flex-wrap: wrap;
            padding: 30px 0px;
        }
        .align-center {
            text-align: center;

            .blue-button {
                margin: 10px 0;
                padding: 5px 30px;
                color: white;
                background-color: $brandColor;
                font-size: 16px;
                border-radius: 2px;
                text-transform: uppercase;
                border: none;
            }
        }
    }

    .absolute {
        position: absolute;
        top: -25px;
        left: 105px;
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