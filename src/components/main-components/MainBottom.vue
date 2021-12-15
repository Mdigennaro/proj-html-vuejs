<template>
  <div class="main_bottom_mdg">
    <div class="container_mdg">
      <section class="main_top_news_mdg">

        <img src="../../assets/img/page-logo-1.png" alt="logo">
        <h2>Today's University News</h2>
        <p>Covering topics from classes to politics and student organization events.</p>

        <div class="divisore_mdg"></div>

      </section>

      <section class="main_bottom_news_mdg">
        
        <div 
        v-for="(item, index) in news" 
        :key="index" 
        class="box_news">
            <img :src="require(`../../assets/img/${item.image}.jpg`)" alt="">
            
            <div class="info_news">
              <h4>{{item.title}}</h4>

              <p>By <span>{{item.creator}}</span> | {{item.date}}</p>

              <div class="news_link">
                <span>Read More <i class="fas fa-chevron-right"></i> </span>
                <span><i class="far fa-comments"></i> {{item.comment}}</span>
              </div>

            </div>
          
        </div>

      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainBottom",

  props:{
    news: Array
  }
}
</script>

<style lang="scss">
@import '../../assets/style/utilities.scss';
@import '../../assets/style/vars.scss';
@import '../../assets/style/mixins.scss';

.main_bottom_mdg{
  height: 725px;
  padding: 80px;
  background-color: #f7f5f4;


  .main_top_news_mdg{
    text-align: center;
    color: $primary-color;
    font-family: 'Roboto Slab', sans-serif;

    img{
      width: 80px;
      margin-bottom: 20px;
    }
    
    h2{
      font-size: 25px;
    }

    p{
      font-size: 16px;
    }
  }

  .main_bottom_news_mdg{
    @include justifyBeetwen();
    padding-top: 20px;

    .box_news{
      width: 300px;
      height: 315px;
      background-color:$bianco;

      img{
        width: 100%;
      }

      .info_news{
        color: $arancio;
        padding: 20px 15px;
        font-family: 'Roboto Slab', sans-serif;

        h4{
          line-height: 25px;
        }

        p{
          margin-top: 0px;

          span{
            color: $arancio;
            cursor: pointer;
          }
        }

        .news_link{
          @include justifyBeetwen();

          span{
            font-size: 11px;
            font-family: 'Roboto', sans-serif;
            cursor: pointer;
          }
        }
      }
      
    }
  }
}

</style>