<template>
  <div class="main">

    <Jumbotron />
    <MainTop 
    :users="users"
    :values="values"
    />
    <MainCenter :sections="sections" />

  </div>
</template>

<script>
import Jumbotron from './main-components/Jumbotron.vue';
import MainTop from './main-components/MainTop.vue';
import MainCenter from './main-components/MainCenter.vue';

export default {
  name: "Main",

  components:{
    Jumbotron,
    MainTop,
    MainCenter
  },

  data(){
    return{
      //Main Top
      users:[
        {
          icon: 'fas fa-globe',
          profilo:'International focus',
          text:' - our students come from across the globe'
        },
        {
          icon: 'fas fa-graduation-cap',
          profilo:'Residential courses',
          text:' - we encourage learning and growth'
        },
        {
          icon: 'far fa-address-book',
          profilo:'People not profits',
          text:' - education is a right not a privilege'
        },
      ],

      values:[
        {
          icon:'fas fa-plus',
          text: 'our mission'
        },
        {
          icon:'fas fa-plus',
          text: 'our philosophy'
        },
        {
          icon:'fas fa-plus',
          text: 'our commitment'
        },
        {
          icon:'fas fa-plus',
          text: 'our promise'
        },
        {
          icon:'fas fa-plus',
          text: 'our values'
        },
      ],
      
      //Main Center
      sections:[
        {
          image:'home_courses_section_bg',
          info:'courses',
          add: 'View More'
        },
        {
          image:'home_events_section_bg',
          info:'events',
          add: 'View More'
        },
        {
          image:'home_latest_news_section_bg',
          info:'latest news',
          add: 'View More'
        },
      ]

    }
  }
}
</script>

<style>

</style>