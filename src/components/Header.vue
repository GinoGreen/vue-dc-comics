<template>
   <header class="container">
      <div class="logo">
         <img src="../assets/img/dc-logo.png" alt="logo">
      </div>
      <ul>
         <li v-for="(section, index) in navBar" :key="index">
            <!-- cambio classe active al click -->
            <a 
               :class="{active : (index === activeSection)}" 
               href="#"
               @click="activeSection = index"
            >{{ section }}</a>
         </li>
      </ul>
   </header>
</template>

<script>
export default {
   name: 'Header',
   data() {
      return {
         navBar: ['characters', 'comics', 'movies', 'tv', 'games', 'collectibles', 'videos', 'fans', 'news', 'shop'],
         activeSection: 1
      }
   }
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   header {
      height: 120px;

      @include center('align');
      justify-content: space-between;

      .logo img{
         width: 100px;
      }

      ul {
         @include reset-list;
         @include center('align');

         li a {
            @include reset-a;
            &:hover,
            &:active {
               @include reset-a;
            }
            &:hover {
               border-bottom: 5px solid $brand_color;
            }
            &.active {
               color: $brand_color;
               border-bottom: 5px solid $brand_color;
            }

            padding: 45px 0;
            margin: 0 1.2rem;

            color: #1C1C1C;
            font-size: 1rem;
            font-weight: bold;
            text-transform: uppercase;
         }
      }
   }

</style>