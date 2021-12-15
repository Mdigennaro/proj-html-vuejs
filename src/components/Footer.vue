<template>
  <footer>
    <FooterTop />
    <FooterBottom />
  </footer>
</template>

<script>
import FooterTop from './footer-components/FooterTop.vue';
import FooterBottom from './footer-components/FooterBottom.vue';

export default {
  name: "Footer",

  components:{
    FooterTop,
    FooterBottom
  }
}
</script>

<style>

</style>