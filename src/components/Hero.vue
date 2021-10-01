<template>
    <section class="jumbotron" :style="`background-image: url(${bgImage})`"></section>
</template>

<script>
export default {
    name : "Hero",
    props: ['bgImage']
}
</script>

<style lang="scss" scoped>
    .jumbotron {
        height: 18.75rem;
        background-size: cover;
        background-repeat: no-repeat;
    }

</style>