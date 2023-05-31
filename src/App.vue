<template>
  <div class="main">
    <NavbarComponent />
    <router-view />    
  </div>
</template>

<script>
import NavbarComponent from '@/components/NavbarComponent.vue'

export default {
  components: {
    NavbarComponent
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Barlow&family=Barlow+Condensed:wght@400;700&family=Bellefair&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 18px;
}

body {
  font-family: sans-serif;
  background: #0b0f1a;
  color: #FFFFFF;
  margin: 0;
  padding: 0;
}

.page{
  min-height: calc(100% - 9.8rem - 6px );
}

.main{
  position: fixed;
  width: 100%;
  height: 100%;
  inset: 0;
  overflow: auto;
}

.container{
  max-width: 1280px;
  margin: 0 auto;
}

a {
  text-decoration: none;
}

.light-color{
  color: #D0D6F9;
}
.dark-color{
  color: #0B0D17;
}

p {
  font-family: 'Barlow';
  font-style: normal;
  font-weight: 400;
  font-size: 1rem;
  line-height: 1.7rem;
}

h1 {
  font-family: 'Bellefair';
  font-style: normal;
  font-weight: 400;
  font-size: 8.3rem;
  line-height: 9.5rem;
  text-transform: uppercase;
}

h2 {
  font-family: 'Bellefair';
  font-style: normal;
  font-weight: 400;
  font-size: 5.5rem;
  line-height: 6.4rem;
  text-transform: uppercase;
}

h3 {
  font-family: 'Bellefair';
  font-style: normal;
  font-weight: 400;
  font-size: 3.1rem;
  line-height: 3.5rem;
  text-transform: uppercase;
}

h4 {
  font-family: 'Bellefair';
  font-style: normal;
  font-weight: 400;
  font-size: 1.8rem;
  line-height: 2rem;
  text-transform: uppercase;
}

h5 {
  font-family: 'Barlow Condensed';
  font-style: normal;
  font-weight: 400;
  font-size: 1.5rem;
  line-height: 1.9rem;
  letter-spacing: 0.26rem;
  color: #D0D6F9;
}

.subheading1 {
  font-family: 'Bellefair';
  font-style: normal;
  font-weight: 400;
  font-size: 1.5rem;
  line-height: 1.7rem;
  text-transform: uppercase;
}

.subheading2 {
  font-family: 'Barlow Condensed';
  font-style: normal;
  font-weight: 400;
  font-size: 0.8;
  line-height: 0.9rem;
  letter-spacing: 0.13rem;
  text-transform: uppercase;
}

.back {
    position: fixed;
    inset: 0;
    z-index: -2;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      position: absolute;
      inset: 0;
    }
  }
</style>