<template>
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
  </div>
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

  .footer_bottom_mdg{
    height: 80px;

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
</style>