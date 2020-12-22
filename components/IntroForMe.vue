<template>
  <b-row id="My-Intro-Banner" class="p-2">
    <b-col md="auto">
      <img
        id="Me"
        thumbnail
        rounded="circle"
        src="@/assets/Photos/Introduction/me.jpg"
        alt="A photo of the sites delveoper standing on a Mauna Kea"
      />
    </b-col>
    <b-col>
      <h1>Hello There,</h1>
      <p id="Description-Text">
        I'm Keli'i McCrary, and you caught me in progress designing this
        tutorial. Please feel free to check out what is currently available
        right now as more will be added soon!
      </p>
    </b-col>
  </b-row>
</template>

<style scoped>
* {
  box-sizing: border-box;
}
#My-Intro-Banner {
  width: 100%;
  background: #2f80ed;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  color: #fcfcfc;
  margin: 0;
}

#Description-Text {
  font-size: 24px;
}

#Me {
  height: 10rem;
  border-radius: 100%;
}
</style>
