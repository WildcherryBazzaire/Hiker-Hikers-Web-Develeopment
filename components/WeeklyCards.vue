<template>
  <NuxtLink :to="link">
    <b-card class="Weekly-Cards">
      <div
        :style="{ backgroundImage: `url(${backgroundImage})` }"
        class="Background-Wrapper"
      ></div>
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
    link: {
      default: '/',
      type: String,
    },
  },
}
</script>

<style scoped>
.Weekly-Cards {
  overflow: hidden;
  position: relative;
  display: flex;
  min-height: 14rem;
  justify-content: center;
  align-items: center;
  border-radius: 1rem;
  text-align: center;
  color: #fcfcfc;
  background-color: rgba(0, 0, 0, 0);
  transition: transform 0.55s ease 0.05s;
}

.Background-Wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0%;
  left: 0%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  z-index: -1;
  transition: transform 0.55s ease 0.05s;
}

.Weekly-Cards:hover {
  transform: scale(1.05, 1.05);
}

.Weekly-Cards:hover .Background-Wrapper {
  transform: scale(1.2);
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
  z-index: 2;
}
</style>
