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

<style>

</style>