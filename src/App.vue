<template>
  
  <nav-bar />
  <router-view />
</template>

<script>
// import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/partials/NavBar.vue';

export default {
  name: 'app',
  components: {
    NavBar,
  },
  data() {
    return {}
  }

}
</script>

<style>
  body {
    background-color: white;
  }
</style>
