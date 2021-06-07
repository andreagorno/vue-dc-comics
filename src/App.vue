<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <!-- header start -->
    <Header />
    <!-- /header start -->

    <!-- main start -->
    <Main />
    <!-- /main start -->

    <!-- footer start -->
    <Footer />
    <!-- /footer start -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"


export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Patua+One&family=Staatliches&display=swap');


* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Patua One', cursive;
}
</style>
