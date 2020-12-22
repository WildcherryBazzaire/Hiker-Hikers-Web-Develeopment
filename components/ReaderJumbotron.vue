<template>
  <b-jumbotron
    id="Jumbotron"
    :style="{ backgroundImage: `url(${image})` }"
    fluid
    text-variant="white"
  >
    <b-img class="Hint-Down" :src="require('@/assets/Widgets/expand.svg')">
    </b-img>
    <b-navbar fluid class="Jumbotron-Menu">
      <b-navbar-brand class="Jumbotron-Menu-Items">
        {{ text.credit }}
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
    <template #header>{{ text.title }}</template>
    <template #lead>
      {{ text.subtitle }}
    </template>
  </b-jumbotron>
</template>

<script>
export default {
  props: {
    image: {
      default() {
        return {}
      },
      type: Object,
    },
    text: {
      default() {
        return {
          title: 'Add a Title Here',
          subtitle: 'Add a subtitle Here!',
          credit: 'Add credit here!',
        }
      },
      type: Object,
    },
  },
}
</script>

<style scoped>
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
  background-attachment: fixed;
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

.Hint-Down {
  position: absolute;
  left: 48.5%;
  height: 2.5rem;
  top: 95%;
  -webkit-animation: animation 1500ms linear infinite both;
  animation: animation 1500ms linear infinite both;
}

@-webkit-keyframes animation {
  0% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  6.57% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  6.67% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  9.67% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      4.853,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 4.853, 0, 1);
  }
  12.67% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      8.8,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 8.8, 0, 1);
  }
  15.68% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      10.874,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 10.874, 0, 1);
  }
  18.61% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      11.392,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 11.392, 0, 1);
  }
  26.02% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      10.323,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 10.323, 0, 1);
  }
  29.76% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.941,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.941, 0, 1);
  }
  33.23% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.846,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.846, 0, 1);
  }
  33.33% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.846,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.846, 0, 1);
  }
  33.43% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.675,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.675, 0, 1);
  }
  36.2% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      4.733,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 4.733, 0, 1);
  }
  39.07% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      1.147,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1.147, 0, 1);
  }
  41.94% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.542,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.542, 0, 1);
  }
  44.81% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.925,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.925, 0, 1);
  }
  48.24% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.639,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.639, 0, 1);
  }
  52.22% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.195,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.195, 0, 1);
  }
  59.63% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0.061,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0.061, 0, 1);
  }
  63.12% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0.041,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0.041, 0, 1);
  }
  73.33% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.004,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.004, 0, 1);
  }
  74.44% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.004,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.004, 0, 1);
  }
  89.32% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  100% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
}

@keyframes animation {
  0% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  6.57% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  6.67% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  9.67% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      4.853,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 4.853, 0, 1);
  }
  12.67% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      8.8,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 8.8, 0, 1);
  }
  15.68% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      10.874,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 10.874, 0, 1);
  }
  18.61% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      11.392,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 11.392, 0, 1);
  }
  26.02% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      10.323,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 10.323, 0, 1);
  }
  29.76% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.941,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.941, 0, 1);
  }
  33.23% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.846,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.846, 0, 1);
  }
  33.33% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.846,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.846, 0, 1);
  }
  33.43% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      9.675,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 9.675, 0, 1);
  }
  36.2% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      4.733,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 4.733, 0, 1);
  }
  39.07% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      1.147,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1.147, 0, 1);
  }
  41.94% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.542,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.542, 0, 1);
  }
  44.81% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.925,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.925, 0, 1);
  }
  48.24% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.639,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.639, 0, 1);
  }
  52.22% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.195,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.195, 0, 1);
  }
  59.63% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0.061,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0.061, 0, 1);
  }
  63.12% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0.041,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0.041, 0, 1);
  }
  73.33% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.004,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.004, 0, 1);
  }
  74.44% {
    -webkit-transform: matrix3d(
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      0,
      0,
      1,
      0,
      0,
      -0.004,
      0,
      1
    );
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, -0.004, 0, 1);
  }
  89.32% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
  100% {
    -webkit-transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
    transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  }
}
</style>
