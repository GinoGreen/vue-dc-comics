<template>
   <main>

      <section id="jumbotrone">

      </section>

      <section id="thumbs" class="container">
         <TemplateCard
            v-for="(card, index) in Cards"
            :key="index"
            :card="card"
         />
      </section>

      <button>load more</button>

   </main>
</template>

<script>

import Cards from '../assets/data/Cards';
import TemplateCard from './TemplateCard';

export default {
   name: 'Main',
   components: {
      TemplateCard
   },
   data() {
      return {
         Cards
      }
   }
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   main {
      padding-bottom: 20px;
      background-color: #1C1C1C;
      @include center();
      flex-direction: column;
      
      #jumbotrone {
         width: 100%;
         height: 530px;
         background-image: url('../assets/img/jumbotron.jpg');
         background-size: cover;
         background-position: top;
         background-repeat: no-repeat;
      }

      #thumbs {
         display: flex;
         flex-wrap: wrap;
      }

      button {
         padding: 8px 50px;

         color: #fff;
         font-size: 1rem;
         font-weight: bold;
         text-transform: uppercase;

         border: none;
         background-color: $brand_color;
      }
   }
</style>