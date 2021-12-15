<template>
  <div class="main">

    <Jumbotron />
    <MainTop 
    :users="users"
    :values="values"
    />
    <MainCenter :sections="sections" />
    <MainBottom 
    :news="news"/>

  </div>
</template>

<script>
import Jumbotron from './main-components/Jumbotron.vue';
import MainTop from './main-components/MainTop.vue';
import MainCenter from './main-components/MainCenter.vue';
import MainBottom from './main-components/MainBottom.vue';

export default {
  name: "Main",

  components:{
    Jumbotron,
    MainTop,
    MainCenter,
    MainBottom
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
      ],

      //Main Bottom
      news:[
        {
          image:'news_single_post_header_1',
          title:'What do successful grads think you should study?',
          creator: 'admin',
          date:'March 16th, 2016',
          comment: 0
        },
        {
          image:'news_single_post_header_2',
          title:'Former student discusses success in the fashion industry',
          creator: 'admin',
          date:'March 15th, 2016',
          comment: 0
        },
        {
          image:'news_single_post_header_3',
          title:'How do you best prepare for university?',
          creator: 'admin',
          date:'March 15th, 2016',
          comment: 0
        },
      ]
    }
  }
}
</script>

<style>

</style>