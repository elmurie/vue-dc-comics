<template>
  <div id="app">
    <div>
      <Header/>
      <Hero/>
      <Content/>
      <CallToAction/>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Content from './components/Content.vue'
import CallToAction from './components/CallToAction.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Content,
    CallToAction,
    Footer
  }
}
</script>

<style lang="scss">
  @import './assets/style/common';
  
  #app {
    width: 100%;
  }
  
</style>
