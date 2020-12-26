<template>
  <b-container class="Root-Container" fluid>
    <!-- Where the jumbotron is -->
    <reader-jumbotron :image="JumbotronMenu.image" :text="JumbotronMenu.text">
    </reader-jumbotron>
    <b-container>
      <b-row>
        <b-col sm="12">
          <p>Under Development! Come back soon!</p>
        </b-col>
        <template v-for="(items, index) in sections">
          <text-section :key="items.sectionTitle" :section-content="items">
            <template v-if="index == 0">
              <h3>HTML</h3>
              <p>
                Is the language that provides various elements that allows to
                layout the structure and flow of a website. These elements may
                include text, images, links, element containers(known as divs),
                forms, and many more you will discover when completing future
                modules or more complex websites. Additionally, scripts created
                within CSS & JS will be referenced and linked to HTML scripts as
                this is what our website is.
              </p>
              <h3>CSS</h3>
              <p>
                CSS allows for better visual representation of default styles
                that are defined by a specific internet browser. Everything from
                color and font-size to media queries which will allow for
                different visuals depending on screen size and even fake HTML
                elements called pseudo-elements that will be useful soon in
                upcoming modules.
              </p>
              <h3>JavaScript(JS)</h3>
              <p>
                Other than just web design, this language can be used to code
                various other things you can think of that can be done in other
                languages(e.g Ct.js). It is for that JS will be handling the
                logic of our web applications and whatever info that is external
                to it.
                <br /><br />
                Although HTML already has pre-built logic for elements, it is
                very limited and not as powerful to more advanced queries which
                include HTTP requests to API and including node packages.
              </p>
            </template>
          </text-section>
        </template>
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
        image: require('@/assets/Photos/Week_One/building.jpg'),
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
            source: require('@/assets/Photos/Week_One/elements.jpeg'),
            creatorCaption: 'Photo by ...',
            context:
              '"A journey of a thousand miles is started by taking the first step." ~ Chiense Proverb',
          },
          contentText:
            'Let’s get down to brass tacks, these languages are what make every website you see on the internet. No matter how fancy and technical it gets, it all boils down to these 3 computer languages. They each play their own role in how a website looks and functions, and are necessary to learn as they compose the minimal building blocks on what all the other modules stand upon.',
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
