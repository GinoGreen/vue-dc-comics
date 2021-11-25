<template>
   <div class="myCard">
      <div class="img-square-container">
         <img :src="card.thumb" :alt="card.series">
      </div>
      <h5>{{ card.series }}</h5>
   </div>
</template>

<script>
export default {
   name: 'TemplateCard',
   props: {
      card: Object
   }
}
</script>
// via giulio petroni 33b
// via troscana 32

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   .myCard {
      width: calc(100% / 6 - 40px);
      margin: 25px 20px;

      cursor: pointer;

      .img-square-container {
         // fix immagine sempre quadrata
         width: 100%;
         padding-top: 100%;

         position: relative;

         overflow: hidden;

         img {
            width: 100%;

            display: block;

            position: absolute;
            top: 0;
            left: 0;
            
         }
      }

      h5 {
         margin-top: 20px;
         font-size: .9rem;
         color: #fff;
      }
   }

</style>