<template>
  <header class="container">
      <div class="section-logo">
          <img src="../assets/dc-logo.png" alt="">
      </div>
      <div class="section-nav">
          <ul>
              <li v-for="(link, index) in links" :key="index">
                  <a :href="link.url" :class="{ active: link.current }"> {{ link.text }} </a>
              </li>
          </ul>
      </div>
  </header>
</template>

<script>
export default {
    name: "Header",

    data: function() {
        return {
            links: [
                {
                    text: "characters",
                    url:"#characters",
                    current: false
                },
                {
                    text: "comics",
                    url:"#comics",
                    current: true
                },
                {
                    text: "movies",
                    url:"#movies",
                    current: false
                },
                {
                    text: "tv",
                    url:"#tv",
                    current: false
                },
                {
                    text: "games",
                    url:"#games",
                    current: false
                },
                {
                    text: "collectibles",
                    url:"#collectibles",
                    current: false
                },
                {
                    text: "videos",
                    url:"#videos",
                    current: false
                },
                {
                    text: "fans",
                    url:"#fans",
                    current: false
                },
                {
                    text: "news",
                    url:"#news",
                    current: false
                },
                {
                    text: "shop",
                    url:"#shop",
                    current: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import "../style/variables";

    header {
        display: flex;
        align-items: center;
        // background-color: aquamarine;
    }

    .section-logo {
        flex-grow: 1;
        
        img {
            height: 80px;
            margin: 20px 0;
        }
    }
    .section-nav {
        height: 125px;

        ul {
            list-style: none;

            li {
            display: inline-block;
            margin: 0 10px;
            font-size: 16px;
            text-transform: uppercase;
            line-height: 120px;
            
            cursor: pointer;

                a {
                    color: #52565B;
                    display: inline-block;
                    height: calc(100% - 5px);
                    text-decoration: none;

                    &.active,
                    &:hover {
                        color: $brandColor;
                        border-bottom: 5px solid $brandColor;
                    }
                }
            }
        }   
    }
    
</style>