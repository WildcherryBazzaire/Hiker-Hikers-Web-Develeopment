<template>
  <NuxtLink to="/reader">
    <b-card
      :style="{ backgroundImage: `url(${backgroundImage})` }"
      class="Weekly-Cards"
    >
      <b-card-body class="Weekly-Cards-Body">
        <h2>{{ cardTitle }}</h2>
      </b-card-body>
    </b-card>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    cardTitle: {
      default: 'Insert Name',
      type: String,
    },
    backgroundImage: {
      default: '',
      type: String,
    },
  },
}
</script>

<style scoped>
.Weekly-Cards {
  overflow: hidden;
  display: flex;
  min-height: 14rem;
  justify-content: center;
  align-items: center;
  border-radius: 1rem;
  text-align: center;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  color: #fcfcfc;
}

a:hover {
  text-decoration: none;
}

.card-body {
  flex: 0;
}

.Weekly-Cards-Body {
  margin: auto;
  flex: 0;
}
</style>
