<template>
   <div class="back">
      <img src="@/assets/destination/background-destination-desktop.jpg" alt="">
   </div>
   <section class="section container">
      <div class="left">
         <CanvasPlanet material="moon.jpg"/>
      </div>
      <div class="rigth">
         <h2>MOON</h2>
      </div>
   </section>
</template>

<script>
import CanvasPlanet from '@/components/CanvasPlanet.vue'

export default {
   components: {
      CanvasPlanet
   }
};
</script>

<style scoped lang="scss">
   .section{
      display: flex;

      .left{
         width: 100%;
      }
   }
</style>