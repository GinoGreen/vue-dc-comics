<template>
   <div class="myCard">
      <img :src="card.thumb" :alt="card.series">
      <!-- <h5>{{ card.series }}</h5> -->
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

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   .myCard {
      width: calc(100% / 6 - 40px);
      margin: 0 20px;

      cursor: pointer;

      img {
         width: 100%;
         // height: calc(50%);

         display: block;

         object-fit: cover;
         object-position: top;
      }

      h5 {
         margin-top: 20px;
         font-size: .9rem;
         color: #fff;
      }
   }

</style>