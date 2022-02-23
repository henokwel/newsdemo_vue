<template>
  <section id="headlineContainer">
    <!-- <ArticleCard :item="" /> -->
    <div id="topHeadline">
      <!-- big card -->
      <div id="bigHeadline" v-for="(post, index) in reverseArticles" :key="index">
        <ArticleCard :item="post" :mediaCard="true" />
      </div>

      <!-- small card with horizontal scroll -->
      <div id="bigHeadlineText">
        <div v-for="(post, index) in headlineArticles" :key="index">
          <ArticleCard :miniCard="true" :miniMedia="true" :item="post" />
        </div>
      </div>
    </div>

    <div id="miniHeadline">
      <!-- Media Cards-->
    </div>
  </section>
</template>


<script>
import ArticleCard from "./ArticleCard.vue";
export default {
  components: { ArticleCard },
  props: {
    headlineArticles: Array,
  },

  computed:{
    reverseArticles(){
       let newArt =  this.headlineArticles
       return newArt.slice(15).reverse()
    }
  },
   data() {
    return {
      stories: [
        {
          author: "The Editorial Board",
          title: "WSJ: New Cold War Arrives...",
          description:
            "WSJ: New Cold War Arrives  (Top headline, 4th story, link)  Related stories:PUTIN STAKES CLAIM TO VAST NEW TERRITORY. 'REMINISCENT OF HITLER' 'Peacekeeping' tanks roll into Ukraine...\r\nZelensky hints at pursuing nukes...\r\nHow Bid…",
          content:
            "Who in the Lords name does Putin think gives him the right to declare new so-called countries? President Biden asked Tuesday in announcing new sanctions against Russia. The answer is a complacent Wes… [+373 chars]",
        },
      ],
      topHeadline: this.headlineArticles,

      miniHeadline: this.headlineArticles,
    };
  },
};
</script>




<style scoped>
#headlineContainer {
  grid-area: headline;
  margin-left: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-right: 1px solid #bcbcbc;

  /* background: beige; */
  /* border: 2px solid; */
}

#bigHeadline {
  margin-bottom: 30px;
}
#topHeadline {
  /* background: greenyellow; */
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center; */
  width: 100%;
  /* padding: 10px; */
}
#bigHeadlineText {
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;

  /* overflow-y: hidden;
  overflow-x: scroll; */
}
</style>