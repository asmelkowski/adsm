<template>
  <v-app id="app">
    <navbar />
    <nuxt />
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue';

export default {
  components: {
    Navbar,
  },
  data () {
    return {
    }
  }
}
</script>

<style>
#app {
  background: url("~assets/xbg.jpg") no-repeat center center;
  /* background-size: cover; */
}
</style>
