<template>
   <nav class="navbar">
      <img class="logo" src="@/assets/shared/logo.svg" alt="">
      <div class="box_line">
         <span class="line"></span>
      </div>
      <ul class="nav_list">
         <li class="active">
            <router-link to="/">
               <strong>00</strong>
               <p>HOME</p>
            </router-link>
         </li>
         <li><router-link to="/about">
               <strong>01</strong>
               <p>DESTINATION</p>
            </router-link>
         </li>
         <li><router-link to="/about">
               <strong>02</strong>
               <p>CREW</p>
            </router-link>
         </li>
         <li><router-link to="/about">
               <strong>03</strong>
               <p>TECHNOLOGY</p>
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
   margin: 40px 0;
   position: relative;

   .logo {
      margin: 0px 40px;
   }


   .box_line {
      width: 100%;
      
      .line {
         height: 1px;
         width: 100%;
         background: #FFFFFF;
         mix-blend-mode: normal;
         opacity: 0.25;
         position: absolute;
         top: 52px;
         left: 220px;
         z-index: 2;
      }
   }

   .nav_list {
      display: flex;
      list-style: none;
      align-items: center;
      gap: 50px;
      background: rgba(255, 255, 255, 0.04);
      backdrop-filter: blur(40.7742px);
      padding: 0 120px;



      span {
         font-weight: 700;
      }

      a {
         display: flex;
         gap: 10px;
         font-style: normal;
         font-size: 16px;
         line-height: 19px;
         letter-spacing: 2.7px;
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
         padding: 43px 0 40px 0;
         border-bottom: 3px solid transparent;
         transition: all .3s;
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