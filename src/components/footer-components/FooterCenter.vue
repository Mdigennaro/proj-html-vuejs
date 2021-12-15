<template>
  <div class="footer_center_mdg">
    
    <div class="container_footer_mdg">

      <div class="avada_university">
        <nav>
          <h5>Avada university</h5>

          <ul>
            <li 
            v-for="(item, index) in info"
            :key="index">
            <i :class="item.icon"></i>{{item.text}}</li>
          </ul>

        </nav>
      </div>

      <div class="recent_posts">

        <nav>
          <h5>Recent Posts</h5>

          <ul>
            <li
            v-for="(post, index) in posts"
            :key="index" 
            >
            <div class="title_post">
              <i :class="post.icon"></i><p>{{post.text}}</p>
            </div>
            <span>{{post.date}}</span></li>
          </ul>
        </nav>

      </div>

      <div class="links">
        <nav>

          <h5>Courses</h5>

          <ul>
            <li
            v-for="(course, index) in courses"
            :key="index" 
            >
            {{course}}
            </li>
          </ul>

        </nav>

        <nav>

          <h5>admissions</h5>

          <ul>
            <li
            v-for="(admission, index) in admissions"
            :key="index" 
            >
            {{admission}}
            </li>
          </ul>

        </nav>

        <nav>

          <h5>resources</h5>

          <ul>
            <li
            v-for="(resource, index) in resources"
            :key="index" 
            >
            {{resource}}
            </li>
          </ul>

        </nav>

        <nav>

          <h5>quickLinks</h5>

          <ul>
            <li
            v-for="(quickLink, index) in quickLinks"
            :key="index" 
            >
            {{quickLink}}
            </li>
          </ul>

        </nav>

      </div>

      <div class="upcoming_events">

        <nav>
          <h5>upcoming events</h5>

          <ul>
            <li 
            v-for="(event, index) in events"
            :key="index">
              <div class="box_date_events">
                <div class="box_date_letter">
                  <span>Fri</span>
                </div>
                <span>27</span>
              </div>
              <div class="box_events">
                <p>{{event.title}}</p>
                <span>{{event.date}}</span>
                <span>{{event.state}}</span>
              </div>
            </li>
            <li>View More...</li>
          </ul>
        </nav>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "FooterCenter",

  props:{
    info: Array,
    posts: Array,
    courses: Array,
    admissions: Array,
    resources: Array,
    quickLinks: Array,
    events: Array
  }
}
</script>

<style lang="scss">
@import '../../assets/style/utilities.scss';
@import '../../assets/style/mixins.scss';
@import '../../assets/style/vars.scss';

  .footer_center_mdg{
    height: 450px;
    background-image: url(../../assets/img/university_ft_bg.png);
    background-size: cover;
    background-position-y: center;
    border-bottom: 1px solid #e2e6f1;

    .container_footer_mdg{
      width: 90%;
      padding-top: 70px;
      margin: 0 auto;
      @include justifyBeetwen();

      .avada_university, .recent_posts, .links, .upcoming_events{
        width: 250px;
        nav{

          h5{
            font-size: 12px;
            font-family: 'Roboto', sans-serif;
            color: $primary-color;
            text-transform: uppercase;
            margin-bottom: 30px
          }

          ul{
            @include column();
          }
        }
      }

      .avada_university{
        li{
          color: #94979f;
          font-size: 12px;            
          line-height: 16px;
          i{
            margin-right: 15px;
          }
              
        }

        li:nth-of-type(2), li:nth-of-type(3){
          margin-left: 14px;
        }

        li:nth-of-type(5){
          color: $primary-color;
              
          i{
            color: #94979f;
          }
        }

        li:nth-of-type(n + 4){
          margin-top: 10px;
        }
      }

      .recent_posts{
        li{
          padding: 10px 0;
          border-bottom: 1px solid #e2e6f1;
          .title_post{
            display: flex;
            color: $primary-color ;

            i{
              margin-right: 5px;
              font-size: 8px;
              margin-top: 7px;
            }

            p{
              margin: 0px;
              font-size: 12px;
              color: $primary-color ;
              cursor: pointer;
            }
          }

          span{
            margin-top: 0px;
            padding-left: 10px;
            color: #94979f;
            font-size: 12px;            line-height: 16px;
            font-family: 'Roboto', sans-serif;
          }
        }
        li:first-of-type{
          padding-top: 0px;
        }
      }

      .links{
        width: 500px;
        height: 400px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;

        li{
          font-size: 13px;
          color: $primary-color ;
          cursor: pointer;
          font-family: 'Roboto',sans-serif;
          line-height: 20px;
          margin-right: 0 20px;
          
        }
        li:last-of-type{
          margin-bottom: 30px;
        }
      }

      .upcoming_events{
        li{
          font-size: 13px;
          color: $primary-color ;
          cursor: pointer;
          font-family: 'Roboto',sans-serif;
          line-height: 20px;
          display: flex;
          padding-bottom: 5px;
          margin-bottom: 20px;
          border-bottom: 1px solid #e2e6f1;

        }
          
        li:last-of-type{
          border-bottom: none;
        }

        .box_date_events{
          height: 50px;
          width: 42px;
          background-color: $arancio;
          padding: 1px;
          text-align: center;
          margin-right: 20px;

          .box_date_letter{
            width: 35px;
            height: 28px;
            background-color: #f3f4f7;
            margin:1px auto;
            @include alignCenter();
            justify-content: center;

            span{
              color:$arancio;
              text-transform: uppercase;
              font-size: 10px;
              font-weight: bold;
            }
          }

          span{
            color: $bianco;
            font-weight: bold;
            font-size: 12px;
          }
        }

        .box_events{
          display: flex;
          flex-direction: column;
          p{
            color: $primary-color;
            font-family: 'Roboto Slab', sans-serif;
            margin: 0;
            line-height: 10px;
            margin-bottom: 10px;
          }

          span{
            margin: 0px;
            line-height: 18px;
            font-size: 10px;
            color: #94979f ;
            cursor: pointer;
          }
        }

      }
    }
  }
</style>