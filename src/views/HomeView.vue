<template>
  <daily-headline />
  <quick-read />
  <opinion-section />
</template>


<script>
// @ is an alias to /src

 import DailyHeadline from "@/components/DailyHeadline.vue";
import OpinionSection from "@/components/OpinionSection.vue";
import QuickRead from "@/components/QuickRead.vue";

export default {
  name: "HomeView",
  components: {
     DailyHeadline,
    OpinionSection,
    QuickRead,
  },
};
</script>



<style>
#app {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: 80px auto;
  grid-template-areas:
    "nav nav nav"
    "quickR headline opinion";

  margin: 0 5% 0 5%;
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #2c3e50;
  min-height: 100vh;
}

nav {
  grid-area: nav;
}
</style>
