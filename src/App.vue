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
  margin: 0 1% 0 1%;
}

    /* Responsivnes________  

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  #app {
    /* background: rgb(204, 96, 114); */
    margin: 0 4% 0 4%;
  }
}
/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (max-width: 992px) {
  #app {
    /* background: orange; */

    grid-template-columns: 2fr 1.3fr;
    grid-template-areas:
      "nav nav"
      ". . "
      "headline quickR"
      "opinion  quickR";
  }
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 760px) {
  #app {
    /* background: blanchedalmond; */
    grid-template-columns: 2fr;

    grid-template-areas:
      "nav "
      ". "
      "headline"
      "opinion"
      "quickR";
  }
}
</style>
