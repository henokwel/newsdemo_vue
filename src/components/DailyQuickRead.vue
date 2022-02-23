<template>
  <div id="quickRContainer">
    <!-- <h1>Quick Read</h1> -->

    <div v-for="post in quickReadArticles" :key="post.id">
      <ArticleCard :item="post" />
    </div>
  </div>
</template>


<script>
import ArticleCard from "./ArticleCard.vue";
export default {
  components: { ArticleCard },
  props: {
    quickReadArticles: Array,
  },
};
</script>
<style scoped>
#quickRContainer {
  grid-area: quickR;
  height: fit-content;

  display: flex;
  flex-direction: column;
  align-items: center;

  padding-right: 20px;
  padding-left: 15px;
  border-right: 1px solid #bcbcbc;
  /* height: 100%; */

  /* border: 2px solid; */
  /* background-color: rgb(141, 87, 127); */
}

/* Responsivnes________  */

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
}
</style>


}