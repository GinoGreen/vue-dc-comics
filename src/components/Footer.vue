<template>
   <footer>

      <div class="lists">
         <div class="container bg-dc-logo">
         


         </div>
      </div>

      <div class="bottom-footer">
         <div class="container">



         </div>
      </div>

   </footer>
</template>

<script>
export default {
   name: 'Footer'
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/vars.scss';

   footer .lists {
      background-image: url('../assets/img/footer-bg.jpg');

      .bg-dc-logo {
         padding: 40px 0;
         background-image: url('../assets/img/dc-logo-bg.png');
         background-position: right;
         background-repeat: no-repeat;
      }
   }

   footer .bottom-footer {
      height: 20px;
      background-color: #303030;
   }

</style>