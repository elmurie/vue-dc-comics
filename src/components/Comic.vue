<template>
    <div class="comic">
        <img class="comic__cover" :src="card.thumb" :alt="card.series" >
        <div class="comic__name">{{card.series}}</div>
    </div>
</template>

<script>
export default {
    name : "Comic",
    props : ['card']
}
</script>

<style lang="scss" scoped>
    .comic {
        width: calc( (100% / 6) - 10px);
        margin: .625rem .3125rem; 
        
        .comic__cover {
            width: 9.375rem;
            height: 9.375rem;
            object-fit: cover;
            object-position: top;
            transition: .5s;

            &:hover {
                cursor: pointer;
                transform: scale(1.1);
            }
        }
        .comic__name {
            margin-top: .3125rem;
            text-transform: uppercase;
            font-size: .9375rem;
        }
    }

</style>