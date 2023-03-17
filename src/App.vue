<template>
  <div class="app">
    <NavBar />
    <router-view />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
  },
};
</script>

<style>
.app {
  padding: 3rem;
  height: 100vh;
  width: 100vw;
  background-image: linear-gradient(
      to top,
      rgba(126, 213, 111, 0.8),
      rgba(40, 180, 133, 0.8)
    ),
    url(./assets/chiled.jpg);
  background-size: cover;
  background-position: top;
  color: #eee;
}

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
}

body {
  box-sizing: border-box;
  font-family: "Lato", sans-serif;
  font-weight: 400;
  color: #777;
  line-height: 1.7;
}
</style>
