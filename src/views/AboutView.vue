<template>
  <DailyHeadline :headlineArticles="headlineArticles" />
  <QuickRead :quickReadArticles="quickReadArticles" />
  <OpinionSection :opinionArticles="opinionArticles" />
</template>

<script>
// @ is an alias to /src

import DailyHeadline from "@/components/DailyHeadline.vue";
import OpinionSection from "@/components/DailyOpinion.vue";
import QuickRead from "@/components/DailyQuickRead.vue";
import NewData from "../../data.json";
export default {
  name: "GlobalView",
  components: {
    DailyHeadline,
    OpinionSection,
    QuickRead,
  },

  data() {
    return {
      headlineArticles: [],
      opinionArticles: [],
      quickReadArticles: [],
    };
  },
  created() {
    this.getData();
  },
  methods: {
    async getData() {
      try {
        const res = await fetch(
          `https://newsapi.org/v2/everything?q=apple&from=2022-02-23&to=2022-02-23&sortBy=popularity&apiKey=${process.env.VUE_APP_NEWS_API_KEY}`
        );
        const data = await res.json();

        this.headlineArticles = await data.articles;
        this.opinionArticles = await data.articles;
        this.quickReadArticles = await data.articles;

      } catch (error) {
        
        this.headlineArticles = NewData;
        this.opinionArticles = NewData;
        this.quickReadArticles = NewData;
      }
    },
  },
};
</script>

 



<style>
</style>
