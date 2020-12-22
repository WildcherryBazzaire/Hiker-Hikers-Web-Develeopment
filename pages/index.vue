<template>
  <b-container class="Root-Container" fluid>
    <intro-for-me />
    <b-row class="Weekly-Categories px-5">
      <b-col sm="12">
        <h2 class="mt-5">Week One</h2>
      </b-col>
      <template v-for="items in cards">
        <b-col :key="items.title" class="mx-4 mt-3" sm="12" md="3">
          <weekly-cards
            :card-title="items.title"
            :background-image="items.backgroundImage"
            :link="items.link"
          />
        </b-col>
      </template>
      <b-col sm="12">
        <h2 class="mt-5">Week Two</h2>
      </b-col>
      <b-col class=" " sm="12">
        <p>More will be added here soon...</p>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import IntroForMe from '@/components/IntroForMe'
import WeeklyCards from '@/components/WeeklyCards'
export default {
  components: {
    'intro-for-me': IntroForMe,
    'weekly-cards': WeeklyCards,
  },
  data() {
    return {
      cards: [
        {
          title: 'Intro',
          backgroundImage: require('@/assets/Photos/Week_One/The_Basics.jpg'),
          link: '/reader',
        },
        {
          title: 'First Webpage',
          backgroundImage: require('@/assets/Photos/Week_One/building.jpg'),
          link: '/reader2',
        },
      ],
    }
  },
}
</script>

<style>
.Root-Container {
  margin: 0 auto;
  min-height: 100vh;
  padding: 0;
  overflow-x: hidden;
}

.Weekly-Categories {
  text-align: center;
  justify-content: center;
}
</style>
