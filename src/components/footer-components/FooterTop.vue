<template>
  <div class="footer_top_mdg">
    <div class="container_mdg">
      <img src="../../assets/img/footer_top.png" alt="numero iscrizioni">

      <div class="form_mdg">
        <input type="text" placeholder="Name">
        <input type="text" placeholder="Email">
        <input type="text" placeholder="Telephone">
        <button>apply now</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterTop"
}
</script>

<style lang="scss">
@import '../../assets/style/vars.scss';
@import '../../assets/style/utilities.scss';
@import '../../assets/style/mixins.scss';

  .footer_top_mdg{
    height: 310px;
    background-color: $primary-color;  
    @include alignCenter();

    .container_mdg{
      @include alignCenter();
      flex-direction: column;
      justify-content: center;

      img{
        width: 725px;
        margin-top: -40px;
      }

      .form_mdg{
        width: 100%;
        @include justifyBeetwen();
        padding: 20px;

        input{
          background-color: #444d63;
          border: none;
          line-height: 30px;
          padding-left: 12px;
          color: $bianco;
          font-family: 'Roboto', sans-serif;
          font-size: 12px;
          width: 230px;
        }

        button{
          width: 175px;
        }
      }
    }
    

  }
</style>