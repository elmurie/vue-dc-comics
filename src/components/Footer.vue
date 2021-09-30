<template>
    <footer>
        <div class="container">
            <div class="footer-top">
                <ul>
                    <li v-for="(list, index) in lists" :key="index">{{list.title}}
                        <ul class="bigList">
                            <li>
                                <a href="list.url" v-for="(link, position) in list.links" :key="position">{{link.linkName}}</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="footer-bottom">
                <div class="lx">
                    <button>SIGN-UP NOW!</button>
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
            lists : [
                {
                    title :  "COMICS",
                    links : [
                        { linkName : "Characters", url : "#"},
                        { linkName: "Comics", url : "#" },
                        { linkName: "Movies", url : "#" },
                        { linkName: "TV", url : "#" },
                        { linkName: "Games", url : "#" },
                        { linkName: "Videos", url : "#" },
                        { linkName: "News", url : "#" }
                    ]
                },
                {
                    title : "SHOP",
                    links : [
                        { linkName : "Shop DC", url : "#"},
                        { linkName : "Shop DC Collectibles", url : "#"}
                    ]
                },
                {
                    title : "DC",
                    links : [
                        { linkName : "Terms Of Use", url : "#"},
                        { linkName : "Privacy Policy (New)", url : "#"},
                        { linkName : "Ad Choices", url : "#"},
                        { linkName : "Advertising", url : "#"},
                        { linkName : "Jobs", url : "#"},
                        { linkName : "Subscriptions", url : "#"},
                        { linkName : "Talent Workshops", url : "#"},
                        { linkName : "CPSC Certificates", url : "#"},
                        { linkName : "Ratings", url : "#"},
                        { linkName : "Shop Help", url : "#"},
                        { linkName : "Contact us", url : "#"}
                    ]
                },
                {
                    title : "SITES",
                    links : [
                        { linkName : "DC", url : "#"},
                        { linkName : "MAD Magazine", url : "#"},
                        { linkName : "DC Kids", url : "#"},
                        { linkName : "DC Universe", url : "#"},
                        { linkName : "DC Power Visa", url : "#"}
                    ]
                },
                
            ],
            logos : [
                {logoName: "Facebook", logoSrc : require('@/assets/img/footer-facebook.png'), url : "#"},
                {logoName: "Twitter", logoSrc : require('@/assets/img/footer-twitter.png'), url : "#"},
                {logoName: "YouTube", logoSrc : require('@/assets/img/footer-youtube.png'), url : "#"},
                {logoName: "Pinterest", logoSrc : require('@/assets/img/footer-pinterest.png'), url : "#"},
                {logoName: "Periscope", logoSrc : require('@/assets/img/footer-periscope.png'), url : "#"}
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .bigList {
        display: flex;
        flex-direction: column;
        flex-wrap : wrap;
    }
    .bigList li {
        display: flex;
        flex-direction: column;
    }
</style>