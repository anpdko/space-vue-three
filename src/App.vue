<template>
  <NavbarComponent/>
  <router-view />
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
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
  background: #0b0f1a;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

a {
  text-decoration: none;
}
</style>