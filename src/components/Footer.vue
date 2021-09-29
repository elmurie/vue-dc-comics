<template>
    <footer>
        <div class="container">
            <ul>
                <li v-for="(list, index) in lists" :key="index">{{list.title}}
                    <ul>
                        <li>
                            <a href="list.url" v-for="(link, position) in list.links" :key="position">{{link.linkName}}</a>
                        </li>
                    </ul>
                </li>
            </ul>
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
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>