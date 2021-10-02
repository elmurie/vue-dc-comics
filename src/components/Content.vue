<template>
    <section>
        <div class="current-series container">
            <div class="flag">CURRENT SERIES</div>
			<Comic v-for="(comic,index) in comics" :key="index" :card="comic"/>
            <a>LOAD MORE</a>
        </div>
    </section>
</template>

<script>
import Comic from '../components/Comic.vue';
import albums from '../data/dc-comics.json';

export default {
    name : "Content",
    components : {
        Comic
    },
    data() {
        return {
            comics :  albums
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';
    section {
        background-color: #1C1C1C;
        color: #fff;
        padding: 2.5rem;
        
        .current-series {
            position: relative;
            display: flex;
            flex-wrap: wrap;

            .flag {
                position: absolute;
                top: -14%;
                font-size: 1.5625rem;
                font-weight: 700;
                background-color : $mainColor;
                padding: .3125rem;
            }

            a {
                font-size: 15px;
                font-weight: 700;
                background-color : $mainColor;
                padding: .625rem 3.125rem;
                margin: 0 auto;
                transition: .3s;

                &:hover {
                    cursor: pointer;
                    transform: scale(1.2);
                }
            }
        }
    }

</style>