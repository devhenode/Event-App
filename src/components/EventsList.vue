<template>

  <div class="events container">
    <h2 class="subtitle is-3">Check out our upcoming events</h2>
    <div class="columns is-multiline">
      <div
        v-for="event in events"
        :event="event"
        :key="event.id" 
        class="column is-one-quarter"
      >
        <router-link :to="'/event/' + event.id">
          <EventCard :event="event" />
        </router-link>
      </div>
    </div>

    <!-- <div class="columns is-multiline">
      <div class="column is-one-quarter">
        <EventCard />
      </div>
    </div>

    <div class="columns is-multiline">
      <div class="column is-one-quarter">
        <EventCard />
      </div>
    </div>

    <div class="columns is-multiline">
      <div class="column is-one-quarter">
        <EventCard />
      </div>
    </div> -->
  </div>

</template>
<script>
  import EventCard from './EventCard.vue';
  export default {
    name: 'EventsList',
    components: {
      EventCard,
    },
    data() {
      return {
        event: {},
        events: [
          {
            id: 1,
            name: 'Charity Ball',
            category: 'Fundraising',
            description:
              'Spend an elegant night of dinner and dancing with us as we raise money for our new rescue farm.',
            featuredImage: 'https://media.istockphoto.com/id/991732782/photo/close-up-of-sommelier-serving-red-wine-at-fine-dining-restaurant.jpg?s=2048x2048&w=is&k=20&c=xii8e4HeDJP6lN2uKjEIxwBWomv6ZsoO6VNWm1NT_R4=',
            images: [
              'https://better.net/wp-content/uploads/2023/10/Gala-SFBallet-DEV19GAL_NR014-770x514.jpg',
              'https://better.net/wp-content/uploads/2023/10/Gala-SFBallet-DEV19GAL_NR014-770x514.jpg',
              'https://better.net/wp-content/uploads/2023/10/Gala-SFBallet-DEV19GAL_NR014-770x514.jpg',
            ],
            location: '1234 Fancy Ave',
            date: '12-25-2019',
            time: '11:30',
          },
          {
            id: 2,
            name: 'Rescue Center Goods Drive',
            category: 'Adoptions',
            description:
              'Come to our donation drive to help us replenish our stock of pet food, toys, bedding, etc. We will have live bands, games, food trucks, and much more.',
            featuredImage: 'https://cached.imagescaler.hbpl.co.uk/resize/scaleWidth/952/cached.offlinehbpl.hbpl.co.uk/news/NST/GPFrGalas-2016100303590713.jpg',
            images: ['https://placekitten.com/500/500'],
            location: '1234 Dog Alley',
            date: '11-21-2019',
            time: '12:00',
          },
        ]
      }
    }
  };
</script>
<style lang="scss" scoped>
  .events {
    margin-top: 100px;
    text-align: center;
  }
</style>