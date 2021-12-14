<template>
  <header>

    <HeaderTop 
    :contacts="contacts" 
    :socials="socials"
    />
    <!-- passo l'array al figlio headerBottom salvandolo con la voce menu-->
    <HeaderBottom :menu="menu"/>

  </header>
</template>

<script>
//import
import HeaderTop from './header-components/HeaderTop.vue';
import HeaderBottom from './header-components/HeaderBottom.vue';

export default {
  name: "Header",

  components:{
    HeaderTop,
    HeaderBottom
  },

    data(){
    return{
      contacts:[
        {
          icon:'fas fa-phone',
          text: '1.800.567.8910' ,
          add:'24hrs'
        },
        {
          icon:'fas fa-envelope',
          text: 'Contact Us',
          add:''
        },
        {
          icon:'fas fa-graduation-cap',
          text: 'Alumni',
          add:''
        },
        {
          icon:'fas fa-university',
          text: 'Campus',
          add:''
        },
      ],

      socials:['fab fa-facebook-f', 'fab fa-twitter', 'fab fa-youtube', 'fab fa-instagram'],

      menu:[
        {
          url: '/',
          text: 'home',
          add: '',
          active: true
        },
        {
          url: '/',
          text: 'about',
          add: '',
          active: false
        },
        {
          url: '/',
          text: 'courses',
          add: 'new',
          active: false
        },
        {
          url: '/',
          text: 'events',
          add: '',
          active: false
        },
        {
          url: '/',
          text: 'facilities',
          add: '',
          active: false
        },
        {
          url: '/',
          text: 'news',
          add: '',
          active: false
        },
        {
          url: '/',
          text: 'admissions',
          add: 'apply',
          active: false
        },
      ],
    }
  }
}
</script>

<style lang="scss">

  header{
    height: 133px;
    font-family: 'Roboto', sans-serif;
  }

</style>