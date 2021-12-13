<template>
  <div class="header_top">
   
    <div class="container_mdg">
      <div class="header_tl">
        <nav>
          <ul>
            <li 
            v-for="(contact, index) in contacts"
            :key="index"
            >
              <a href=""><i :class="contact.icon"></i>{{contact.text}}<span :class="{bordo : contact.add !== ''}" >{{contact.add}}</span></a>
            </li>
          </ul>
        </nav>
      </div>
      <div class="header_tr">
        <nav>
          <ul>
            <li 
            v-for="(social, index) in socials"
            :key="index"
            ><a href=""><i :class="social"></i></a></li>
          </ul>
        </nav>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name:"HeaderTop",

  props:{
    contacts: Array,
    socials: Object
  }
}
</script>

<style lang="scss">
@import "../assets/style/mixins.scss";

  .header_top{
    height: 30%;
    background-color:#f09a3f;
    @include alignCenter();
    font-size: 9px;
    
    .container_mdg{
      @include justifyBeetwen();

      .header_tl{

        li{
          margin-right: 15px;

          a{
            color: white;
            font-size: 10px;

            .bordo{
              background-color: #d48129;
              border-radius: 2px;
              font-size: 7px;
              padding:3px 5px;
              margin-left: 5px;
            }

            i{
              font-size: 10px;
              margin-right: 5px;
            }
          }
        }
      }

      .header_tr{

        i{
          color: white;
          font-size: 12px;
          margin: 0 8px;
        }
      }
    }

  }

</style>