<template>
  <b-container class="Root-Container" fluid>
    <intro-for-me />
    <b-row class="mt-5 Weekly-Categories px-5">
      <b-col sm="12">
        <h2>Week One</h2>
      </b-col>
      <template v-for="items in cards">
        <b-col :key="items.title" class="mx-4 mt-3" sm="12" md="3">
          <weekly-cards />
        </b-col>
      </template>
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
      cards: [{ title: 'win!' }],
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
