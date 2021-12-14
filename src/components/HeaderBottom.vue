<template>
  <div class="header_bottom">

    <div class="container_mdg">
      <div class="logo_mdg">
        <img src="../assets/img/university_logo.png" alt="logo">
      </div>
      <div class="menu_mdg">

        <nav>
          <ul>
            <!-- Creo un ciclo con la prop e do la classe bordo solo quando item add-contiene un elemento -->
            <li 
            v-for="(item, index) in menu" :key="index"><a @click="item.active == !item.active" :class="{active: item.active}" :href="item.url">{{item.text}}</a><span :class="{bordo : item.add !== ''}" >{{item.add}}</span></li>
          </ul>
        </nav>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "HeaderBottom",

  //prendo l 'array menu che si trova in header
  props:{
    menu: Array
  }
}
</script>

<style lang="scss">
//importo le mixins e le vars
@import "../assets/style/mixins.scss";
@import "../assets/style/vars.scss";

.header_bottom{
  height: 70%;
  @include alignCenter();

  .container_mdg{
    @include justifyBeetwen();

    .logo_mdg img{
      width: 170px;
    }

    .menu_mdg{
      @include alignCenter();
      text-transform: uppercase;

      li{
        margin:0 15px;
        font-size: 11px;
        font-weight: bold;
        a{
          color: $primary-color;
        }

        a:hover{
          color: $arancio;
        }
        
        .active{
          color: $arancio;
        }

        .bordo{
          vertical-align: middle;
          margin: 0 7px;
          font-size: 8px;
          padding: 2px 6px;
          background-color: $azzurro;
          border-radius: 3px;
          color:$bianco;
        }
        
      }
      li:last-of-type{
        margin-right:0px;
      }
    }
  }
}

</style>