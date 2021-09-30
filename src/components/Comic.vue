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
        margin: 0 .3125rem; 
        
        .comic__cover {
            width: 150px;
            height: 150px;
            object-fit: cover;
            object-position: top;
        }
        .comic__name {
            text-transform: uppercase;
            font-size: .9375rem;
        }
    }

</style>