<template>
   <section class="shortcut">

      <div class="container">

         <div class="row">

            <div class="thumb col-lg-2 col-md-3 offset-lg-1 offset-3">
               <img src="../assets/img/buy-comics-digital-comics.png" alt="digital comics">
               <h4>digital comics</h4>
            </div>
            <div class="thumb col-lg-2 col-md-3">
               <img src="../assets/img/buy-comics-merchandise.png" alt="digital comics">
               <h4>dc merchandise</h4>
            </div>
            <div class="thumb col-lg-2 col-md-3">
               <img src="../assets/img/buy-comics-shop-locator.png" alt="digital comics">
               <h4>comic shop locator</h4>
            </div>
            <div class="thumb col-lg-2 col-md-3 offset-lg-0 offset-md-3">
               <img src="../assets/img/buy-comics-subscriptions.png" alt="digital comics">
               <h4>subscription</h4>
            </div>
            <div class="thumb col-lg-2 col-md-3">
               <img src="../assets/img/buy-dc-power-visa.svg" alt="digital comics">
               <h4>dc power visa</h4>
            </div>

         </div>

      </div>

   </section>
</template>

<script>
export default {
   name: 'Shortcut'
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   section.shortcut {
      background-color: $brand_color;

      .thumb {
         height: 60px;
         margin-top: 40px;
         margin-bottom: 40px;

         @include center('align');

         img {
            height: 100%;
         }

         img[src$=".svg"] {
            width: 60px;
         }

         h4 {
            padding-left: 10px;
            margin: 0;

            color: #fff;
            font-size: 14px;
            text-transform: uppercase;
         }

      }
   }

</style>