<template>
  <footer>
    <FooterTop />
    <FooterCenter :info="info"
    :posts="posts"
    :courses="courses"
    :admissions="admissions"
    :resources="resources"
    :quickLinks="quickLinks"
    :events="events"
    />
    <FooterBottom  :infoLinks="infoLinks"
    :socials="socials"
    />
  </footer>
</template>

<script>
import FooterTop from './footer-components/FooterTop.vue';
import FooterCenter from './footer-components/FooterCenter.vue';
import FooterBottom from './footer-components/FooterBottom.vue';

export default {
  name: "Footer",

  components:{
    FooterTop,
    FooterCenter,
    FooterBottom
  },

  data(){
    return{
      //Footer Center
      info:[
        {
          icon: 'fas fa-home',
          text: 'Residential Location'
        },
        {
          icon: '',
          text: '9521 Broadsberry Avenue'
        },
        {
          icon: '',
          text: 'Paddington RC7 9ZA'
        },
        {
          icon: 'fas fa-phone',
          text: '1.800.458.556'
        },
        {
          icon: 'far fa-envelope',
          text:'info@your-domain.com'
        },
        {
          icon: 'far fa-clock',
          text:'Monday - Friday: 8:00 AM - 10:00 PM'
        },
      ],

      posts:[
        {
          icon: 'fas fa-chevron-right',
          text: 'What do succesful grads think you should study?',
          date: 'March 16, 2016'
        },
        {
          icon: 'fas fa-chevron-right',
          text: 'Former student discusses success in the fashion industry',
          date: 'March 15, 2016'
        },
        {
          icon: 'fas fa-chevron-right',
          text: 'How do you best prepare for university?',
          date: 'March 15, 2016'
        },
      ],

      courses:[
        'Arts & Humanities', 'Businnes & Management', 'Engineering & Technology', 'Life Sciences & Medicine', 'Natural Sciences'
      ],

      admissions:[
        'Eligibility', 'Application', 'Review Process', 'How to Apply'
      ],

      resources:[
        'Camous Directory', 'Academic Calendar', 'Sport Clubs', 'Graduate Programs', 'Faculty & Staff'
      ],

      quickLinks:[
        'University Library', 'Campus Srvices', 'Careers'
      ],

      events:[
        {
          title: 'Business Seminar',
          date:'July 1, 2019 @ 8:00 am - july 1, 2021 @ 5:00 pm',
          state:'United States'
        },
        {
          title: 'Politics Seminar',
          date:'November 6, 2019 @ 8:00 am - November 6, 2021 @ 5:00 pm',
          state:'United Kingdom'
        }
      ],

      //Footer Bottom
      infoLinks:[
        {
          link: '© Theme Fusion ',
          dash: '|'
        },
        {
          link: 'All Rights Reserved',
          dash: '|'
        },
        {
          link: 'Powered by WordPress',
          dash: '|'
        },
        {
          link: 'support@theme-fusion.com',
          dash: '|'
        },
        {
          link: '1.800.555.6789',
          dash: ''
        },
      ],

      socials:[
        'fab fa-facebook-f', 'fab fa-twitter', 'fab fa-youtube', 'fab fa-instagram'
      ]
    }
  }
}
</script>

<style>

</style>