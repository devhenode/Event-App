<template>
  <nav class="navbar container" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
        <strong class="is-size-4">Animal Rescue League</strong>
      </a>
      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div id="navbar" class="navbar-menu">
      <div class="navbar-start">
        <router-link to="/" class="navbar-item">Home</router-link>
        <router-link to="/about" class="navbar-item">About</router-link>
      </div>
      <!-- This is the line  -->
      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-dark">
              <strong>Sign In</strong>
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
// import { RouterLink } from 'vue-router'

export default {
}
</script>

<style scoped>
  nav {
    background-color: white;
    margin-top: 2px;
    margin-bottom: 30px;
    a {
      font-weight: bold;
      &.router-link-exact-active {
        color: #d88d00;
      }
    }
  }
</style>