<template>
    <div class="comic">
        <img class="comic__cover" src="comicbook.thumb" alt="comicbook.series" >
        <div class="comic__name">
            {{comicbook.series}}
        </div>

    </div>
</template>

<script>
export default {
    name : "Comic",
    props : ['comicbook']
}
</script>

<style>

</style>