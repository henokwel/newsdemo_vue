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
};
</script>



<style>
 
 
</style>
