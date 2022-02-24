<template>
  <div id="opinionContainer">
    <div id="opinionContainer">
      <div v-for="(post, index) in opinionArticles" :key="index">
        <ArticleCard :item="post" :mediaCard="true" />
      </div>
    </div>
  </div>
</template>



<script>
import ArticleCard from "./ArticleCard.vue";
export default {
  components: { ArticleCard },
  props: {
    opinionArticles: Array,
  },
};
</script>


<style scoped>
#opinionContainer {
  grid-area: opinion;
  /* background: paleturquoise; */
  /* border: 2px solid; */
  margin-left: 10px;
}
</style>