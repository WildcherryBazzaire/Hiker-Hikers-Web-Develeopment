<template>
  <b-card class="Weekly-Cards">
    <b-card-body class="Weekly-Cards-Body">
      <h2>The Basics</h2>
    </b-card-body>
  </b-card>
</template>

<script>
export default {}
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
  background-image: url('~@/assets/Photos/Week_One/The_Basics.jpg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  color: #fcfcfc;
}

.Weekly-Cards-Body {
  margin: auto;
  flex: 0;
}
</style>
