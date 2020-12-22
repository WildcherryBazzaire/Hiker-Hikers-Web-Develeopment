<template>
  <b-container class="Root-Container" fluid>
    <!-- Where the jumbotron is -->
    <!-- <reader-jumbotron :image="JumbotronMenu.image" :text="JumbotronMenu.text">
    </reader-jumbotron> -->
    <b-container>
      <b-row>
        <b-col sm="12">
          <p>Under Development! Come back soon!</p>
        </b-col>
        <!-- <template v-for="items in sections">
          <text-section :key="items.sectionTitle" :section-content="items" />
        </template> -->
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
// import TextSection from '@/components/TextSection'
// import JumboTron from '@/components/ReaderJumbotron'
export default {
  //   components: {
  //     'text-section': TextSection,
  //     'reader-jumbotron': JumboTron,
  //   },
  data() {
    return {
      JumbotronMenu: {
        image: require('@/assets/Photos/Week_One/The_Basics.jpg'),
        text: {
          title: 'The Basics',
          subtitle:
            ' About the website, assumptions about you ,Tutorial structure, goals',
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
</style>
