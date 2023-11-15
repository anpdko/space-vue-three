<template>
   <nav class="navbar">
      <img class="logo" src="@/assets/shared/logo.svg" alt="">
      <span class="line"></span>
      <ul class="menu">
         <li :class="{ active: $route.path === '/' }">
            <router-link to="/">
               <strong>00</strong>
               HOME
            </router-link>
         </li>
         <li :class="{ active: $route.path === '/destination' }">
            <router-link to="/destination">
               <strong>01</strong>
               DESTINATION
            </router-link>
         </li>
         <li :class="{ active: $route.path === '/crew' }">
            <router-link to="/crew">
               <strong>02</strong>
               CREW
            </router-link>
         </li>
         <li :class="{ active: $route.path === '/technology' }">
            <router-link to="/technology">
               <strong>03</strong>
               TECHNOLOGY
            </router-link>
         </li>
      </ul>
   </nav>
</template>

<script>
export default {
   name: 'NavbarComponent',
}
</script>

<style scoped lang="scss">
.navbar {
   display: flex;
   align-items: center;
   padding: 2.2rem 0;
   position: relative;  

   .logo {
      width: 2.7rem;
      height: 2.7rem;
      margin: 0px 2.2rem;
   }

   .line {
      height: 1px;
      width: 50%;
      background: #FFFFFF;
      mix-blend-mode: normal;
      opacity: 0.25;
      transform: translateX(50px);
      z-index: 2;
   }

   .menu {
      min-width: 50%;
      width: 100%;
      display: flex;
      list-style: none;
      align-items: center;
      justify-content: center;
      gap: 50px;
      background: rgba(255, 255, 255, 0.04);
      backdrop-filter: blur(40.7742px);
      padding: 0 2.7rem;

      span {
         font-weight: 700;
      }

      a {
         display: flex;
         gap: 10px;
         font-style: normal;
         font-size: 0.9rem;
         line-height: 1rem;
         letter-spacing: 0.15rem;
         cursor: pointer;
         color: #FFFFFF;
      }

      p {
         font-weight: 200;
      }

      li.active {
         border-bottom: 3px solid white;
      }

      li {
         padding: calc(2.2rem + 3px) 0 2.2rem 0;
         border-bottom: 3px solid transparent;
         transition: all .3s;
         font-family: 'Barlow Condensed';
         font-style: normal;
         font-weight: 400;
         font-size: 0.9rem;
         line-height: 1rem;
         letter-spacing: 2.7px;
      }

      li:hover {
         border-bottom: 3px solid #FFFFFF50;
      }

      li.active:hover {
         border-bottom: 3px solid white;
      }
   }
}
</style>