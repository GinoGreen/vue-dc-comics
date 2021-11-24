<template>
  <div id="app">
    <Header/>
    <Main/>
    <Shortcut/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Shortcut from './components/Shortcut.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Shortcut,
    Footer
  }
}
</script>

<style lang="scss">
  #app {
    overflow-x: hidden;
  }
</style>
