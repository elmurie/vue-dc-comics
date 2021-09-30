<template>
    <section>
        <div class="container">
            <nav>
                <ul>
                    <li v-for="(link, index) in icons" :key="index">
                        <a href=""><img :src="link.imgSrc" :alt="link.text"></a>
                        <a href="">{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </section>
</template>

<script>
export default {
    name : "CallToAction",
    data() {
        return {
            icons : [
                {
                    text : "DIGITAL COMICS",
                    imgSrc : require('../assets/img/buy-comics-digital-comics.png')
                },
                {
                    text : "DC MERCHANDISE",
                    imgSrc : require('../assets/img/buy-comics-merchandise.png')
                },
                {
                    text : "SUBSCRIPTION",
                    imgSrc : require('../assets/img/buy-comics-subscriptions.png')
                },
                {
                    text : "COMIC SHOP LOCATION",
                    imgSrc : require('../assets/img/buy-comics-shop-locator.png')
                },
                {
                    text : "DC POWER VISA",
                    imgSrc : require('../assets/img/buy-dc-power-visa.svg')
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables';
    section {
        padding: 3rem;
        background-color: $mainColor;
    }

    ul, li {
        display: flex;
        justify-content: center;
        align-items: center;
        
        li {
            width: 20%;
            transition: .3s;

            &:hover {
                opacity: .7;
            }

            a {
                color: #fff;
            }
            img {
                width: 2.8rem;
                margin-right: 1rem;
            }
            &:nth-child(4) img {
                width: 2.1rem;
            }
            &:last-child img {
                width: 4rem;
            }

        }
    }

    

</style>