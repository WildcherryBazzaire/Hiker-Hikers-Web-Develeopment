<template>
  <b-container class="Root-Container" fluid>
    <!-- Where the jumbotron is -->
    <reader-jumbotron :image="JumbotronMenu.image" :text="JumbotronMenu.text">
    </reader-jumbotron>
    <b-container>
      <b-row>
        <template v-for="(items, index) in sections">
          <text-section :key="items.sectionTitle" :section-content="items">
            <ol v-if="index == 2">
              <li>
                Week One
                <ul>
                  <li>Making your first website</li>
                  <li>ES6</li>
                  <li>API Calls</li>
                  <li>The workflow pyramid</li>
                  <li>Week 1 Project: Prefacing a web application</li>
                </ul>
              </li>
              <li>
                Week Two
                <ul>
                  <li>Flex Box & CSS Libraries</li>
                  <li>Intro into npm & Node</li>
                  <li>Vue and component based design</li>
                  <li>Building for mobile</li>
                </ul>
              </li>
              <li>
                Week Three
                <ul>
                  <li>Making a game website</li>
                  <li>Setting up users with firebase</li>
                  <li>Adding 3D models to our site</li>
                </ul>
              </li>
            </ol>
          </text-section>
        </template>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import TextSection from '@/components/TextSection'
import JumboTron from '@/components/ReaderJumbotron'
export default {
  components: {
    'text-section': TextSection,
    'reader-jumbotron': JumboTron,
  },
  data() {
    return {
      JumbotronMenu: {
        image: require('@/assets/Photos/Week_One/The_Basics.jpg'),
        text: {
          title: 'Start Here',
          subtitle:
            ' About the website, assumptions about you ,Tutorial structure',
          credit: "Photo by Keli'i McCrary",
        },
      },
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
            'Hello, and welcome to the website! This is dedicated to the absolute beginner’s and a benchod who wants to take their web development skills from absolute zero to web guru within the insane time frame of 3 weeks. I personally say to those who aren’t full time college students, the time proposed seems rather insane, so feel free to take it at your own paste. However, breaks are only so long, and why not spend on more learning(absolute masochist)! ',
        },
        {
          sectionTitle: 'Assumptions about you',
          contentImage: {
            source: require('@/assets/Photos/Week_One/sun-gazing.jpg'),
            creatorCaption: 'Photo by a friend',
            context: '',
          },
          contentText:
            'Within the 3 weeks, this website will cover the vital essentials of Web design that will help you get off the ground in designing your own professional websites without the need of paying for tools such as WIX. Learning how to design your own websites from scratch will also give additional flexibility in adding a lot of features these tools can’t such as loading 3D models(more on that soon) and fetching information from various API’s. \n\n Covering these topics will also be bundled by various exercises and a weekly project along with that are optional, but recommended as to get a better understanding and grasp of the concept. Anyone can read and understand what’s going on, but it’s a whole other thing to put it into practice, just like driving a car!',
        },
        {
          sectionTitle: 'Tutorial Structure',
          contentText: 'The course will be structured in as follows:',
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
</style>
