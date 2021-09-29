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
                    text : "DIGITAL COMICS",
                    imgSrc : '../img/buy-comics-digital-comics.png'
                },
                {
                    text : "DIGITAL COMICS",
                    imgSrc : '../img/buy-comics-digital-comics.png'
                },
                {
                    text : "DIGITAL COMICS",
                    imgSrc : '../img/buy-comics-digital-comics.png'
                },
                {
                    text : "DIGITAL COMICS",
                    imgSrc : '../img/buy-comics-digital-comics.png'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>