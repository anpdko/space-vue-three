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

.page {
  min-height: calc(100% - 9.8rem - 6px);
}

.main {
  position: fixed;
  width: 100%;
  height: 100%;
  inset: 0;
  overflow: auto;
}

.container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 40px;
}

a {
  text-decoration: none;
}

p {
  font-family: 'Barlow';
  font-style: normal;
  font-weight: 400;
  font-size: 1rem;
  line-height: 1.7rem;
  color: #D0D6F9;
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

.typography {
  font-family: 'Barlow Condensed';
  font-style: normal;
  font-weight: 400;
  font-size: 1.5556rem;
  line-height: 1.8889rem;
  letter-spacing: 0.2625rem;
  text-transform: uppercase;
  padding-block: 2.7rem;

  span {
    font-family: 'Barlow Condensed';
    font-style: normal;
    font-weight: 700;
    font-size: 1.5556rem;
    line-height: 1.8889rem;
    letter-spacing: 0.2625rem;
    color: #FFFFFF;
    mix-blend-mode: normal;
    opacity: 0.25;
    margin-right: 20px;
  }
}

.flex{
  display: flex;
  gap: 100px;
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