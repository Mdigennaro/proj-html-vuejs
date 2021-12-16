<template>

<footer class="footer_bottom">

  <div class="footer_bottom_mdg">
    <div class="container_footer_mdg">

      <div class="link_left">
        <p v-for="(infoLink, index) in infoLinks"
        :key="index"
        >{{infoLink.link}}<span>{{infoLink.dash}}</span></p>
      </div>

      <div class="link_right">
        <nav>
          <ul>
            <li v-for="(social, index) in socials"
            :key="index"
            ><i :class="social"></i></li>
          </ul>
        </nav>
      </div>
        
    </div>

    <div class="box_return">
      <a href=""><i class="fas fa-chevron-up"></i></a>
    </div>
  </div>
</footer>
</template>

<script>
export default {
  name: "FooterBottom",

  props:{
    infoLinks: Array,
    socials: Array
  }
}
</script>

<style lang="scss">
@import '../../assets/style/utilities.scss';
@import '../../assets/style/mixins.scss';
@import '../../assets/style/vars.scss';

  .footer_bottom{
    
    .footer_bottom_mdg{
      height: 80px;
      position: relative;
  
      .container_footer_mdg{
        width: 90%;
        margin: 0 auto;
        @include justifyBeetwen();
  
        .link_left{
          display: flex;
  
          p{
            margin-right: 5px;
            font-size: 10px;
            span{
              margin: 0 10px;
            }
          }
        }
  
        .link_right{
          @include alignCenter();
  
          li{
  
            i{
              margin: 0 7px;
              font-size: 12px;
              color: #bdbfc4;
              cursor: pointer;
            }
          }
  
        }
  
      }
    }
    .box_return{
      position: absolute;
      height: 30px;
      width: 40px;
      background-color: #474747 ;
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
      bottom: 0px;
      right: 55px;
      @include alignCenter();
      justify-content: center;

      i{
        color: $bianco;
      }
    }
  }
</style>