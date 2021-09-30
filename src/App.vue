<template>
  <div id="app">
    <div>
      <Header/>
      <Content/>
      <CallToAction/>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import CallToAction from './components/CallToAction.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    CallToAction,
    Footer
  }
}
</script>

<style lang="scss">
  @import './assets/style/common';
  
</style>
