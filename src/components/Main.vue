<template>
  <div class="main">

    <Jumbotron />
    <MainTop />

  </div>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import MainTop from './MainTop.vue';

export default {
  name: "Main",

  components:{
    Jumbotron,
    MainTop
  }
}
</script>

<style>

</style>