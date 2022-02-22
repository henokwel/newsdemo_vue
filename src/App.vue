<template>
  <nav-header />

  <router-view />
</template>


<script>
// @ is an alias to /src

import NavHeader from "@/components/DailyNav.vue";

export default {
  name: "App",
  components: {
    NavHeader,
  },
};
</script>



<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@700&family=Open+Sans&display=swap");
#app {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: 80px 50px auto;
  grid-template-areas:
    "nav nav nav"
    ". . ."
    "quickR headline opinion";

  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  min-height: 100vh;
  /* background: grey; */
}

nav {
  grid-area: nav;
}
</style>
