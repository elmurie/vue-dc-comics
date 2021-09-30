<template>
    <header>
        <div class="container header-top">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </div>
            <nav>
                <ul>
                    <li v-for="(link, index) in menu" :key="index" :tabindex="index">
                        <a :href="link.url" :class="{ active : link.current }">{{link.text}}</a>
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
@import '../assets/style/variables'; 
    header {
        background-color: #ffffff;
        padding: .9375rem;
        height: 9.375rem;

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;

            ul {
            display: flex;

            li {
                margin: .625rem;

                a {
                    padding: 65px 0;
                    color: #000;
                    font-weight: 700;

                    &:hover {
                        box-shadow: inset -2px -10px 0px -2px $mainColor;
                    }

                    &:focus {
                        box-shadow: inset -2px -10px 0px -2px $mainColor;
                    }

                }
            }
        }


        }
    }
    

</style>