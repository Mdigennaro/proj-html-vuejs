<template>
  <div class="main_center_top_mdg">
    <div 
    v-for="(section, index) in sections" 
    :key="index"
    class="info_main_mdg">

      <img :src="require(`../../assets/img/${section.image}.jpg`)" alt="">

      <div class="sezione_mdg">
        <h2>{{section.info}}</h2>
        <div class="divisore_mdg"></div>
        <span>{{section.add}}</span>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "MainCenter",

  props:{
    sections: Array
  }
}
</script>

<style lang="scss">
@import '../../assets/style/vars.scss';
@import '../../assets/style/utilities.scss';

.main_center_top_mdg{
  height: 570px;
  display: flex;

  .info_main_mdg{
    width: calc(100% / 3);
    overflow: hidden;
    position: relative;

    img{
      width: 100%;
    }

    .sezione_mdg{
      color: $bianco;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;

      h2{
        text-transform: uppercase;
        font-family: 'Roboto Slab', sans-serif;
        font-size: 18px;
      }

      .divisore_mdg{
        width: 45px;
        margin: 20px auto;
      }

      span{
        font-family: 'Roboto', sans-serif;
        font-size: 12px;
        cursor: pointer;
      }
    }
  }
}
</style>