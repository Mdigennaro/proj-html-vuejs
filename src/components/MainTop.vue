<template>
  <div class="main_top">

    <div class="container_mdg">
      <section class="intro_mdg">

        <img src="../assets/img/page-logo-1.png" alt="logo">

        <h2>Inspired By Excellence & Innovation</h2>

        <p>We offer a wide range of high quality of teaching and extra-curricular activities.</p>

        <div class="divisore_mdg"></div>
      </section>

      <section class="offerta_mdg clearfix">
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
          <img src="" alt="">
        </div>
      </section>

    </div>

  </div>
</template>

<script>
export default {
  name: "MainTop"
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

  .main_top{
    height: $h-main;
    @include center();

    .container_mdg{
      height: 500px;
     
      .intro_mdg{
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

      .offerta_mdg{
        
        .proposta_mdg, .intro_video_mdg{
          float: left;
          margin-top: 25px;
        }

        .proposta_mdg{
          width: 58%;
          

          h3{
            color: $primary-color;
            text-transform: uppercase;
            font-family: 'Roboto Slab', sans-serif;
          }

          p{
            margin: 20px 0;
            font-size: 12px;
            line-height: 25px;
            color: #94979f;

          }
        }
        
        .intro_video_mdg{
          width: 42%;
          text-align: right;
          padding-top: 30px;

          img{
            width: 360px;
            height: 200px;
          }

        }
      }
    }
  }
</style>