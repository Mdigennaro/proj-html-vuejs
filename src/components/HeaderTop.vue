<template>
  <div class="header_top">
   
    <div class="container_mdg">
      <div class="header_tl">
        <nav>
          <ul>
            <li><a href=""><i class="fas fa-phone"></i> 1.800.567.8910 <span>24hrs</span></a></li>
            <li><a href=""><i class="fas fa-envelope"></i> Contact Us</a></li>
            <li><a href=""><i class="fas fa-graduation-cap"></i> Alumni </a></li>
            <li><a href=""><i class="fas fa-university"></i> Campus </a></li>
          </ul>
        </nav>
      </div>
      <div class="header_tr">
        <nav>
          <ul>
            <li><a href=""><i class="fab fa-facebook-f"></i></a></li>
            <li><a href=""><i class="fab fa-twitter"></i></a></li>
            <li><a href=""><i class="fab fa-youtube"></i></a></li>
            <li><a href=""><i class="fab fa-instagram"></i></a></li>
          </ul>
        </nav>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name:"HeaderTop"
}
</script>

<style lang="scss">
@import "../assets/style/mixins.scss";

  .header_top{
    height: 30%;
    background-color:#ffab0b;
    @include alignCenter();
    font-size: 9px;
    
    .container_mdg{
      @include justifyBeetwen();

      .header_tr{

        i{
          font-size: 13px;
          margin-right: 0px;
        }
      }
    }

  }

</style>