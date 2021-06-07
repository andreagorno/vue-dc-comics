<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="footer-links">
                    <ul>
                        <li>dc comics</li>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>Tv</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>
                    <ul>
                        <li>dc</li>
                        <li>Term Of Use</li>
                        <li>Privacy policy (New)</li>
                        <li>Ad Choises</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscriptions</li>
                        <li>Talent Workshops</li>
                        <li>CPSC Certificates</li>
                        <li>Ratings</li>
                        <li>Shop Help</li>
                        <li>Contact Us</li>
                    </ul>
                    <ul>
                        <li>Sites</li>
                        <li>Dc</li>
                        <li>MAD Magazine</li>
                        <li>DC Kids</li>
                        <li>DC Universe</li>
                        <li>DC Power Visa</li>
                    </ul>
                    <ul>
                        <li>shop</li>
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>
                    </ul>
                    <div class="footer-logo">
                        <img src="../assets/dc-logo-bg.png" alt="bg-logo">
                    </div>
                </div>
            </div>
            
        </div>
        <div class="footer-bottom">
            <div>
                <div class="sign-up">
                    <span>sign-up now!</span>
                </div>
                
                <span>follow us</span>
                <span><img src="../assets/footer-facebook.png" alt="facebook"></span>
                <span><img src="../assets/footer-twitter.png" alt="twitter"></span>
                <span><img src="../assets/footer-youtube.png" alt="youtube"></span>
                <span><img src="../assets/footer-pinterest.png" alt="pinterest"></span>
                <span><img src="../assets/footer-periscope.png" alt="periscope"></span>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped lang="scss">

    .container {
        width: 80%;
        margin: auto;
    }
    .footer-top {
        display: flex;
        flex-direction: row;
        // height: 300px;
        background-image: url('../assets/footer-bg.jpg');
        background-size: cover;

            .footer-links {
                width: 100%;
                display: flex;
                flex-wrap: wrap;
                // margin-top: 30px; 

                ul {
                    list-style: none; 
                    display: inline-block;
                    margin: 30px 20px 10px 0px;

                    li {
                        font-size: 12px;
                        color: gray;
                        margin: 5px 0;

                        &:first-child {
                            font-size: 18px;
                            text-transform: uppercase;
                            font-weight: bold;
                            margin-bottom: 10px;
                            color: white;
                        }
                    }
                }
                .footer-logo {
                    flex-grow: 1;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    height: 300px;
                    overflow: hidden;

                    img {
                        height: 400px;
                        width: 400px;
                    }
                }
            }

    }

    .footer-bottom {
        background-color: #303030;

        div {
            display: flex;
            width: 80%;
            margin: auto;
            padding: 15px 0;

            .sign-up {
                flex-grow: 1;

                span {
                    color: white;
                    border: 2px solid #0282F9;
                    margin-left: 5px;
                }
            }
            span {
                display: inline-flex;
                align-items: center;
                padding: 5px;
                text-transform: uppercase;

                &:nth-child(2) {
                    color: #0282F9;
                    width: 150px;
                }
            }
        }
    }
</style>