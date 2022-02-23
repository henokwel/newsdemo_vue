<template>
  <daily-headline />
  <quick-read />
  <opinion-section />
</template>

<script>
// @ is an alias to /src

import DailyHeadline from "@/components/DailyHeadline.vue";
import OpinionSection from "@/components/DailyOpinion.vue";
import QuickRead from "@/components/DailyQuickRead.vue";

export default {
  name: "HomeView",
  components: {
    DailyHeadline,
    OpinionSection,
    QuickRead,
  },

  data() {
    return {
      articles: [],
    };
  },
  created() {
    this.getData();
  },
  methods: {
    async getData() {
      const res = await fetch(
        `https://newsapi.org/v2/everything?domains=wsj.com&apiKey=${process.env.VUE_APP_NEWS_API_KEY}`
      );
      const data = await res.json();
      console.log(data);

      if (data.status === "ok") {
        this.articles = data.articles;
      }
    },
  },
};
</script>

 



<style>
</style>
