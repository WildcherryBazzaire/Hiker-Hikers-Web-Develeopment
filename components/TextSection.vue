<template>
  <b-col sm="12">
    <h1 class="text-md-left text-sm-center">
      {{ sectionContent.sectionTitle }}
    </h1>
    <div v-if="sectionContent.contentImage" class="Image-Container">
      <p class="Credit">
        {{ sectionContent.contentImage.creatorCaption }}
      </p>
      <b-img-lazy
        v-if="sectionContent.contentImage.source"
        :src="sectionContent.contentImage.source"
        fluid
        alt="friends"
      />
      <p class="Image-Context mt-1 mb-3 text-md-left text-sm-center">
        {{ sectionContent.contentImage.context }}
      </p>
    </div>
    <p class="text">{{ sectionContent.contentText }}</p>
    <slot></slot>
  </b-col>
</template>

<script>
export default {
  props: {
    sectionContent: {
      default() {
        return {
          sectionTitle: 'What is the title?',
          contentImage: {
            source: '',
            creatorCaption: "Who's it made by?",
            context: "What's it's context?",
          },
          contentText: 'Please enter some text',
        }
      },
      type: Object,
    },
  },
}
</script>

<style scoped>
.Image-Container {
  position: relative;
  color: #fcfcfc;
}

.Image-Context {
  color: #c4c4c4;
}

.Credit {
  position: absolute;
  left: 2%;
  top: 2%;
}

.text {
  font-size: 1.2rem;
}
</style>
