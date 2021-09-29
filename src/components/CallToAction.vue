<template>
    <section>
        <div class="container">
            <nav>
                <ul>
                    <li v-for="(link, index) in icons" :key="index">
                        <img :src="link.imgSrc" :alt="link.text">
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
                    imgSrc : '../img/buy-comics-digital-comics.png'
                },
                {
                    text : "DC MERCHANDISE",
                    imgSrc : '../img/buy-comics-merchandise.png'
                },
                {
                    text : "SUBSCRIPTION",
                    imgSrc : '../img/buy-comics-subscriptions.png'
                },
                {
                    text : "COMIC SHOP LOCATION",
                    imgSrc : '../img/buy-comics-shop-locator.png'
                },
                {
                    text : "DC POWER VISA",
                    imgSrc : '../img/buy-dc-power-visa.svg'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>