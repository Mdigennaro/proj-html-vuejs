<template>
  <header>

    <HeaderTop />
    <HeaderBottom />

  </header>
</template>

<script>
//import
import HeaderTop from './HeaderTop.vue';
import HeaderBottom from './HeaderBottom.vue';

export default {
  name: "Header",

  components:{
    HeaderTop,
    HeaderBottom
  }
}
</script>

<style lang="scss">

  header{
    height: 133px;
    font-family: 'Roboto', sans-serif;
    background-color: violet;
  }

</style>