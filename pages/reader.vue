<template>
  <b-container class="Root-Container" fluid>
    <b-jumbotron id="Jumbotron" fluid text-variant="white">
      <p id="Credit">Photo By Keli'i McCrary</p>
      <template #header>The Basics</template>
      <template #lead>
        What is HTML, Prequisites, Composition of elements, recommended workflow
      </template>
    </b-jumbotron>
    <b-container>
      <b-row>
        <b-col sm="12">
          <h1>What is HTML, CSS, & JS?</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam
            condimentum, erat ac sollicitudin vehicula, velit enim tristique
            magna, sed egestas ex dui vel lacus. Pellentesque eleifend lobortis
            tellus, non egestas quam commodo ornare. Suspendisse finibus, turpis
            nec vulputate suscipit, metus tellus feugiat neque, et sollicitudin
            erat felis bibendum lectus. Vivamus felis mi, blandit ut tellus non,
            accumsan vehicula dolor. In ullamcorper, eros vitae fermentum
            malesuada, lacus nulla posuere nisi, non tempor orci dolor nec
            velit. Etiam facilisis lacinia odio sed semper. Suspendisse
            pellentesque tortor fringilla, blandit lacus cursus, accumsan dui.
            Fusce consectetur nunc a nibh hendrerit fringilla.
          </p>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {}
</script>

<style scoped>
.Root-Container {
  margin: 0 auto;
  min-height: 100vh;
  padding: 0;
}

#Credit {
  position: absolute;
  left: 2%;
  top: 2%;
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
