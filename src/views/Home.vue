<template>
  <!-- <nav-bar /> -->
  <div class="home">
    <section class="hero is-dark">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">Welcome to my Event Management App</h1>
          <h2 class="subtitle">
            Make sure you check out our upcoming events below
          </h2>
          <div class="button-block">
            <button class="button is-xl is-dark">
              Sign Up to Browse Events
            </button>
          </div>
        </div>
      </div>
    </section>

    <EventsList />
  </div>
</template>

<script>
import EventsList from '../components/EventsList.vue';
// import NavBar from '../components/partials/NavBar.vue'

  export default {
    name: 'home',
    components: {
      EventsList,
      // NavBar,
    },

  };
</script>

<style lang="scss" scoped>
  .hero {
    text-align: center;
    background-image: url('https://cdn.auth0.com/blog/vue-meetup/event-banner.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    height: 400px;
  }
  .hero-body .title {
    text-shadow: 4px 4px 4px rgba(0, 0, 0, 0.6);
    padding: 40px 0 20px 0;
    font-size: 60px;
  }
  .subtitle {
    text-shadow: 4px 4px 4px rgba(0, 0, 0, 0.7);
    font-size: 30px;
  }
  .button-block {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    width: 100%;
    position: absolute;
    bottom: -150px;
    .button {
      margin-right: 50px;
      padding-left: 50px;
      padding-right: 50px;
    }
    .welcome {
      width: 400px;
      padding: 10px;
      margin-left: auto;
      margin-right: auto;
    }
  }
  .is-xl {
    font-size: 1.7rem;
  }
</style>
