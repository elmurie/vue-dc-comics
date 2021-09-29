<template>
    <header>
        <div class="container header-top">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </div>
            <nav>
                <ul>
                    <li v-for="(link, index) in menu" :key="index">
                        <a href="link.url" :class="{ active : link.current }">{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name : "Header",
    data () {
        return {
            
        menu : [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .header-top {
        display: flex;
        justify-content: space-between;
        align-items: center;

        ul {
            display: flex;

            li {
                margin: .625rem;
            }
        }
    }

</style>