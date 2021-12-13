<template>
  <div id="app">

    <Header />
    <Main />
    <Footer />

  </div>
</template>

<script>
//IMPORT//
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
//Importo il file che contiene le classi generali o che si potrebbero ripetere
@import "./assets/style/utilities.scss";
@import "./assets/style/mixins.scss";
//importo font awesome
@import "~@fortawesome/fontawesome-free/css/all.css";
//
@import "~@fontsource/roboto/index.css"
</style>
