<template>
   <div class="back" role="img" aria-label="Background Image">
      <img src="@/assets/destination/background-destination-desktop.jpg" alt="background">
   </div>
   <section class="section container page">
      <h4 class="typography"><span>01</span> Pick your destination</h4>
      <div v-for="(planetTab, index) in planetsTab" :key="index" :class="{ active: activeTab === index, flex: true }">
         <div class="left">
            <CanvasPlanet :material="planetTab.materialImg" />
         </div>
         <div class="right">
            <ul class="menu-planet">
               <li v-for="(tab, index) in planetsTab" :key="index" :class="{ active: activeTab === index }"
                  @click="activeTab = index">
                  {{ tab.nameTab }}
               </li>
            </ul>
            <h2>{{ planetTab.title }}</h2>
            <p>{{ planetTab.description }}</p>
            <div class="line"></div>
            <div class="col_info">
               <div>
                  <p>AVG. DISTANCE</p>
                  <h4 class="subheading1">{{ planetTab.distance }}</h4>
               </div>
               <div>
                  <p>Est. travel time</p>
                  <h4 class="subheading1">{{ planetTab.travelTime }}</h4>
               </div>
            </div>
         </div>
      </div>
   </section>
</template>

<script>
import CanvasPlanet from '@/components/CanvasPlanet.vue'
import planets from '@/data/planets'

export default {
   data() {
      return {
         planetsTab: planets,
         activeTab: 0,
      }
   },
   components: {
      CanvasPlanet
   }
};
</script>

<style scoped lang="scss">
.section {
   display: flex;
   flex-direction: column;
   
   .flex {
      display: none;
   }

   .flex.active {
      display: flex;
   }

   .left {
      height: auto;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
   }

   .right {
      display: flex;
      flex-direction: column;
      gap: 30px;

      p {
         max-width: 750px;
      }

      .menu-planet {
         display: flex;
         gap: 35px;

         li {
            list-style: none;
            padding: calc(0.6rem + 2px) 0 0.6rem 0;
            border-bottom: 2px solid transparent;
            transition: all .3s;
            font-family: 'Barlow Condensed';
            font-style: normal;
            font-weight: 400;
            font-size: 0.9rem;
            line-height: 1rem;
            letter-spacing: 2.7px;
            color: #D0D6F9;
            cursor: pointer;
         }

         li:hover {
            border-bottom: 2px solid #FFFFFF50;
         }

         li.active {
            border-bottom: 2px solid white;
         }

         li.active:hover {
            border-bottom: 2px solid white;
         }
      }

      .line {
         width: 100%;
         height: 1px;
         background: #383B4B;
         margin-top: 20px;
      }

      .col_info {
         display: flex;
         gap: 70px;

         p {
            text-transform: uppercase;
            margin-bottom: 10px;
         }
      }
   }
}</style>