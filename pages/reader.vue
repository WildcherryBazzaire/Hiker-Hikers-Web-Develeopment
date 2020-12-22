<template>
  <b-container class="Root-Container" fluid>
    <b-jumbotron id="Jumbotron" fluid text-variant="white">
      <b-navbar fluid class="Jumbotron-Menu">
        <b-navbar-brand class="Jumbotron-Menu-Items">
          Photo By Keli'i McCrary
        </b-navbar-brand>
        <b-navbar-nav class="ml-auto">
          <b-nav-item>
            <b-img
              id="Home-Icon"
              class="Jumbotron-Menu-Items"
              fluid
              sm="1"
              :src="require('@/assets/Widgets/menu.svg')"
            />
          </b-nav-item>
          <b-nav-item>
            <NuxtLink to="/">
              <b-img
                id="Home-Icon"
                class="Jumbotron-Menu-Items"
                fluid
                sm="1"
                :src="require('@/assets/Widgets/home.svg')"
              />
            </NuxtLink>
          </b-nav-item>
        </b-navbar-nav>
      </b-navbar>
      <template #header>Introduction</template>
      <template #lead>
        About the website, assumptions about you ,Tutorial structure, goals
      </template>
    </b-jumbotron>
    <b-container>
      <b-row>
        <template v-for="items in sections">
          <text-section :key="items.sectionTitle" :section-content="items" />
        </template>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import TextSection from '@/components/TextSection'
export default {
  components: {
    'text-section': TextSection,
  },
  data() {
    return {
      sections: [
        {
          sectionTitle: 'About the Course',
          contentImage: {
            source: require('@/assets/Photos/Week_One/amigos.jpg'),
            creatorCaption: 'Photo by a friend',
            context:
              '"A journey of a thousand miles is started by taking the first step." ~ Chiense Proverb',
          },
          contentText:
            'Welcome to the website! It was made to teach others web development through modules that are recommended to be read and done weekly to develop your skills in web development through various exercises and mini-projects. In finishing all the tutorials, you will have a solid understanding of web development along with a really cool portfolio page that you and a friend could have to show off your wicked skills. :D',
        },
        {
          sectionTitle: 'Assumptions about you',
          contentImage: {
            source: require('@/assets/Photos/Week_One/sun-gazing.jpg'),
            creatorCaption: 'Photo by a friend',
            context: '',
          },
          contentText:
            'I assume from the beginning that you’re an absolute beginner and have no previous experience with what this website covers. Additionally, although it is recommended to complete things weekly, it is really up to your pace and can be read within a single day(yikes!) or maybe even a year(no shame in that).',
        },
        {
          sectionTitle: 'Tutorial Structure',
          contentText:
            'The course will be structured into 3 weeks, with each having about 4-5 modules that can be completed throughout. For all the weeks, readings will be followed with a mini-project and then building upon a final project that continues throughout. For the final project, you will be making a portfolio page.',
        },
      ],
    }
  },
}
</script>

<style scoped>
.Root-Container {
  margin: 0 auto;
  min-height: 100vh;
  padding: 0;
}

.Jumbotron-Menu {
  position: absolute;
  width: 100%;
  top: 0%;
  left: 0%;
}

.Jumbotron-Menu-Items {
  color: #fcfcfc;
  fill: #fcfcfc;
}

#Home-Icon {
  height: 2em;
  color: #fcfcfc;
  z-index: 2;
}

#Jumbotron {
  display: flex;
  justify-content: center;
  height: 100vh;
  background-image: url('~@/assets/Photos/Week_One/The_Basics.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  text-align: center;
  position: relative;
}

#Jumbotron > .container {
  display: inline-block;
  margin: auto;
}

#Jumbotron-Title {
  font-size: 16rem;
}
</style>
