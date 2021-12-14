<template>
  <div class="main">

    <Jumbotron />
    <MainTop 
    :users="users"
    :values="values"
    />

  </div>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import MainTop from './MainTop.vue';

export default {
  name: "Main",

  components:{
    Jumbotron,
    MainTop
  },

  data(){
    return{
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
      ]

    }
  }
}
</script>

<style>

</style>