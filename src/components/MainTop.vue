<template>
  <div class="main_top">

    <div class="main_top_intro">

      <div class="container_mdg">
        <section class="intro_top_mdg">

        <img src="../assets/img/page-logo-1.png" alt="logo">

        <h2>Inspired By Excellence & Innovation</h2>

        <p>We offer a wide range of high quality of teaching and extra-curricular activities.</p>

        <div class="divisore_mdg"></div>
        </section>

        <section class="intro_bottom_mdg clearfix">
        <div class="proposta_mdg">
          <h3>why choose avada university?</h3>

          <p>
            We offer a range of training packages in a range of subject areas and can offer blended learning opportunities to best meet your needs. If sitting in a room with a trainer and having the opportunity for discussion with other learners sounds good to you the we can offers this. If you prefer to study in your own time and at your own speed then one of our world class facilities.
          </p>

          <p>
            If you prefer to study in your own time and at your own speed then of our e-learning packages may be right up your street. There is a third option, which is you like the sound of both but perhaps can't attend all training sessions, this is when blended learning comes into its own.
          </p>
        </div>

        <div class="intro_video_mdg">
          <iframe title="vimeo-player" src="https://player.vimeo.com/video/80567526?h=1334ac0d68" width="640" height="360" frameborder="0" allowfullscreen></iframe>
        </div>
        </section>
      </div> 

    </div>

    <div class="main_top_offerta">
      <div class="container_mdg clearfix">
        <div class="user_mdg">
          <h3>World class Facilities</h3>
          <p>
            Avada University is devoted to excellence in teaching, learning, and research, and developing leaders in many disciplines who make a difference globally.
          </p>
          
          <nav>
            <ul>
              <li v-for="(user, index) in users" :key="index">
                <i :class="user.icon"></i>{{user.profilo}}<span>{{user.text}}</span>
              </li>
            </ul>
          </nav>

          <p>
            If you prefer to study in your own time and at your own speed then one of our e-learning packages may be right up your street.
          </p>

        </div>
        
        <div class="valori_mdg">
          <h3>Our Values</h3>
          
          <div 
          v-for="(item, index) in values" 
          :key="index"
          class="offerta_mdg">
            <i :class="item.icon"></i><span>{{item.text}}</span>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "MainTop",

  props:{
    users: Array,
    values: Array
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

  .main_top_intro{
    height: $h-main;
    @include center();

    .container_mdg{
      height: 500px;
     
      .intro_top_mdg{
        text-align: center;
        color: $primary-color;
        font-family: 'Roboto Slab', sans-serif;
        
        img{
          width: 80px;
          margin-bottom: 20px;
        }

        p{
          margin-top: 20px;
          color: #94979f;
          font-size: 15px;
        }

        .divisore_mdg{
          border-bottom: 1px solid $arancio;
          width: 135px;
          margin: 30px auto;
        }
      }

      .intro_bottom_mdg{
        
        .proposta_mdg, .intro_video_mdg{
          float: left;
          margin-top: 25px;
        }

        .proposta_mdg{
          width: 58%;
        }
        
        .intro_video_mdg{
          width: 42%;
          text-align: right;
          padding-top: 30px;

          iframe{
            width: 360px;
            height: 200px;
          }

        }
      }
    }
  }

  .main_top_offerta{
    background-color: #f7f5f4;
    height: 560px;
    @include alignCenter();

    .container_mdg{
      padding-top: 100px;

      .user_mdg, .valori_mdg{
        float: left;
        width: 50%;
        height: 300px;

        ul{
          display: flex;
          flex-direction: column;
        }

        li{
          font-weight: bold;
          color: $primary-color;
          font-family: 'Roboto', sans-serif;
          font-size: 15px;
          line-height: 30px;
          
          i{
            margin: 0 15px;
            color: $arancio;
          }

          span{
            color: #94979f;
            font-weight: normal;

          }
        }

        li:nth-of-type(2) i{
          margin: 0 13px;
        }

        li:nth-of-type(3) i{
          margin: 0 16px;
        }

      }

      .valori_mdg{
        padding-left: 20px;
        
        .offerta_mdg{
          margin-top: 7px;
          color: $arancio;
          background-color: $bianco;
          padding:12px 10px;
        
          i{
            margin: 0 15px;
            font-size: 14px;
          }

          span{
            text-transform: uppercase;
            font-family: 'Roboto', sans-serif;
            font-weight: bold;
            font-size: 12px;
          }
        }

        .offerta_mdg:first-of-type{
          margin-top: 20px;
        }
        
      }

    }
  }
</style>