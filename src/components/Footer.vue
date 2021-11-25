<template>
   <footer>

      <div class="lists">
         <div class="container bg-dc-logo">
            
            <div class="list">
               <h4>dc comics</h4>
               <ul>
                  <li v-for="li in listComics" :key="li.id">
                     <a href="#">{{ li.text }}</a>
                  </li>
               </ul>
            </div>
            <div class="list">
               <h4>dc</h4>
               <ul>
                  <li v-for="li in listDC" :key="li.id">
                     <a href="#">{{ li.text }}</a>
                  </li>
               </ul>
            </div>
            <div class="list">
               <h4>sites</h4>
               <ul>
                  <li v-for="li in listSites" :key="li.id">
                     <a href="#">{{ li.text }}</a>
                  </li>
               </ul>
            </div>
            <div class="list">
               <h4>shop</h4>
               <ul>
                  <li v-for="li in listShop" :key="li.id">
                     <a href="#">{{ li.text }}</a>
                  </li>
               </ul>
            </div>

         </div>
      </div>

      <div class="bottom-footer">
         <div class="container">

            <button>sign-up now!</button>

            <div class="socials">
               <h4>follow us</h4>
               <img src="../assets/img/footer-facebook.png" alt="" class="icon">
               <img src="../assets/img/footer-twitter.png" alt="" class="icon">
               <img src="../assets/img/footer-youtube.png" alt="" class="icon">
               <img src="../assets/img/footer-pinterest.png" alt="" class="icon">
               <img src="../assets/img/footer-periscope.png" alt="" class="icon">
            </div>

         </div>
      </div>

   </footer>
</template>

<script>
export default {
   name: 'Footer',
   data() {
      return {
         listComics:[
            {
               id: 0,
               text: 'Characters',
            },
            {
               id: 1,
               text: 'Comics',
            },
            {
               id: 2,
               text: 'Movies',
            },
            {
               id: 3,
               text: 'TV',
            },
            {
               id: 4,
               text: 'Games',
            },
            {
               id: 5,
               text: 'Videos',
            },
            {
               id: 6,
               text: 'News',
            },
         ],
         listDC:[
            {
               id:7,
               text: 'Term of use',
            },
            {
               id:8,
               text: 'Privacy policy (New)',
            },
            {
               id:9,
               text: 'Ad Choices',
            },
            {
               id:10,
               text: 'Advertising',
            },
            {
               id:11,
               text: 'Jobs',
            },
            {
               id:12,
               text: 'Subscriptions',
            },
            {
               id:13,
               text: 'Talent Workshops',
            },
            {
               id:14,
               text: 'CPSC Certificates',
            },
            {
               id:15,
               text: 'Ratings',
            },
            {
               id:16,
               text: 'Shop help',
            },
            {
               id:17,
               text: 'Contact Us',
            },
         ],
         listSites:[
            {
               id:18,
               text: 'DC',
            },
            {
               id:19,
               text: 'MAD Magazine',
            },
            {
               id:20,
               text: 'DC Kids',
            },
            {
               id:21,
               text: 'DC Universe',
            },
            {
                  d:22,
               text: 'DC Power Visa',
            },
         ],
         listShop:[
            {
               id:23,
               text: 'Shop DC'
            },
            {
               id:24,
               text: 'Shop DC Collectibles'
            },
         ]
      }
   }
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   footer .lists {
      background-image: url('../assets/img/footer-bg.jpg');
      background-repeat: no-repeat;
      background-size: cover;

      .bg-dc-logo {

         display: flex;

         background-image: url('../assets/img/dc-logo-bg.png');
         background-position: right;
         background-repeat: no-repeat;

         .list {
            margin: 40px 20px;

            h4 {
               text-transform: uppercase;
               color: #fff;
            }
            ul {
               @include reset-list;
   
               li a {
                  @include reset-a;
                  color: rgba(255, 255, 255, 0.493);
                  &:hover {
                     @include reset-a;
                     color: rgba(255, 255, 255, 0.493);
                  }
               }
            }
         }
      }
   }

   footer .bottom-footer {
      height: 100px;
      background-color: #303030;

      .container {
         height: 100%;

         @include center('align');
         justify-content: space-between;

         button {
            padding: 12px 20px;

            color: #fff;
            font-size: 1.1rem;
            text-transform: uppercase;

            border: 2px solid $brand_color;
            background-color: transparent;
         }

         .socials {
            @include center('align');

            h4 {
               margin: 0 20px;
               color: $brand_color;
               text-transform: uppercase;
            }

            .icon {
               margin: 0 10px;
               cursor: pointer;
            }
         }
      }
   }

</style>