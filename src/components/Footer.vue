<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="menu">
                    <ul>{{listA.title}}
                        <li v-for="(link, index) in listA.links" :key="index"><a href="#">{{link}}</a></li>
                    </ul>
                    <ul>{{listB.title}}
                        <li v-for="(link, index) in listB.links" :key="index"><a href="#">{{link}}</a></li>
                    </ul>
                    <ul>{{listC.title}}
                        <li v-for="(link, index) in listC.links" :key="index"><a href="#">{{link}}</a></li>
                    </ul>
                </div>
                <!-- <img src="../assets/img/dc-logo-bg.png" alt=""> -->
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="lx">
                <button><a href="#">SIGN-UP NOW!</a></button>
            </div>
            <div class="rx">
                <a>FOLLOW US</a>
                <ul>
                    <li v-for="(logo, logoIndex) in logos" :key="logoIndex">
                        <a :href="logo.url">
                            <img :src="logo.logoSrc" :alt="logo.logoName">
                        </a>
                    </li>
                </ul>
            </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name : "Footer",
    data() {
        return {
            listA : 
                {
                    title :  "DC COMICS",
                    links : [
                        "Characters",
                        "Comics",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News",
                        "SHOP",
                        "Shop DC",
                        "Shop DC Collectibles"
                    ]
                },
            listB : 
                {
                    title : "DC",
                    links : [
                        "Terms Of Use",
                        "Privacy Policy (New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Certificates",
                        "Ratings",
                        "Shop Help",
                        "Contact us"
                    ]
                },
            listC :
                {
                    title : "SITES",
                    links : [
                        "DC",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa"
                    ]
                },

            logos : [
                { logoName: "Facebook", logoSrc : require('@/assets/img/footer-facebook.png'), url : "#" },
                { logoName: "Twitter", logoSrc : require('@/assets/img/footer-twitter.png'), url : "#"},
                { logoName: "YouTube", logoSrc : require('@/assets/img/footer-youtube.png'), url : "#" },
                { logoName: "Pinterest", logoSrc : require('@/assets/img/footer-pinterest.png'), url : "#" },
                { logoName: "Periscope", logoSrc : require('@/assets/img/footer-periscope.png'), url : "#" }
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';
    .footer-top {
        background-image: url('~@/assets/img/footer-bg.jpg/');
        background-size: cover;
        background-repeat: no-repeat;
        padding: 1.25rem;
        .container {
            display: flex;
            justify-content: space-between;

            .menu {
                display: flex;

                ul {
                    margin-right: 1rem;
                    font-size: 1.2rem;
                    color : #fff;
                    font-weight: 700;
                    a {
                        font-size: 1rem;
                        color: #919191;
                    }

                    &:first-child{
                        li:nth-child(8) {
                            a {
                                display: inline-block;
                                font-size: 1.2rem;
                                cursor: initial;
                                color: #fff;
                                font-weight: 700;
                                margin: 1rem 0 .55rem 0;

                            }
                        }
                    }
                }
            }

            
        }
    }
    .footer-bottom {
        background-color: #303030;
        padding: 1.5rem;
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            button {
                background-color: transparent;
                border: .125rem solid $mainColor;
                padding: .9375rem;
                
                & > a{
                    color: white;
                } 
            }
            .lx {
                align-items: center;
            }

            .rx {
                display: flex;
                align-items: center;

                a {
                    margin-right: .625rem ;
                    font-weight: 700;
                    color: $mainColor;
                }

                ul {
                    display: flex;
    
                    li {
                        width: 20%;
                        margin: 3px;

                        img {
                            width: 70%;
                        }
                    }

                }
            }
        }

    }
</style>