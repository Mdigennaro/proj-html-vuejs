<template>
  
  <div class="jumbotron_mdg">
    <div class="box_mdg">
    
      <h1>Inspiring Tomorrows Leaders</h1>
      <h3>The Future Belongs To Those Who See Possibilities Today</h3>

      <div class="bottoni_mdg">

        <button>Find a course</button>
        <button>Apply now</button>
      </div>

    </div>
  </div>

</template>

<script>
export default {
  name: "Jumbotron"
}
</script>

<style lang="scss">
@import "~@fontsource/roboto-slab/400.css";
@import "../assets/style/utilities.scss";
@import "../assets/style/mixins.scss";
@import "../assets/style/vars.scss";


  .jumbotron_mdg{
    height: 650px;
    background-image: url(../assets/img/home_main_slider_bg.jpg);
    background-position-y: -200px;
    background-size: cover;
    @include center();
    text-align: center;
    color: $bianco;

    h1{
      font-size: 55px;
    }

    h3{
      font-size: 20px;
      margin-bottom: 30px;
    }

    .bottoni_mdg{
      
      button{
        margin: 0px 10px;
      }
    }
    
  }

</style>