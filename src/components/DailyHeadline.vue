<template>
  <section id="headlineContainer">
    <!-- <ArticleCard :item="" /> -->
    <div id="topHeadline">
      <!-- big card -->
      <div id="bigHeadline" v-for="(post, index) in topHeadline" :key="index">
        <ArticleCard :item="post" :mediaCard="true" />
      </div>

      <!-- small card with horizontal scroll -->
      <div id="bigHeadlineText">
        <div v-for="(post, index) in miniHeadline" :key="index">
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
    // articles: Array,
  },
  data() {
    return {
      topHeadline: [
        {
          source: {
            id: null,
            name: "Cult of Mac",
          },
          author: "Killian Bell",
          title:
            "Apple tasks South Korean firm with building autopilot chips for its first car",
          description: `Apple will use autopilot chips built by a South Korean firm in its first self-driving
             car, according to a new report. The two companies joined forces around a year ago and are 
            said to be working on a chipset package that is likely to include a CPU, GPU, memor…`,
          url: "https://www.cultofmac.com/767354/apple-car-autopilot-chips/",
          urlToImage:
            "https://cdn.cultofmac.com/wp-content/uploads/2021/12/vanamara-apple-car-concept4.jpg",
          publishedAt: "2022-02-22T14:08:15Z",
          content: `Apple will use autopilot chips built by a South Korean firm in its first
self-driving car, according to a new report.The two companies joined
             self-driving car, according to a new report.The two companies joined
             self-driving car, according to a new report.The two companies joined
             
              forces around a year ago and are said to be working on `,
        },
      ],
      miniHeadline: [
        {
          source: {
            id: null,
            name: "Cult of Mac",
          },
          author: "Killian Bell",
          title:
            "Apple tasks South Korean firm with building autopilot chips for its first car",
          description: `Apple will use autopilot chips built by a South Korean firm in its first self-driving
             car, according to a new report. The two companies joined forces around a year ago and are 
            said to be working on a chipset package that is likely to include a CPU, GPU, memor…`,
          url: "https://www.cultofmac.com/767354/apple-car-autopilot-chips/",
          urlToImage:
            "https://cdn.cultofmac.com/wp-content/uploads/2021/12/vanamara-apple-car-concept4.jpg",
          publishedAt: "2022-02-22T14:08:15Z",
          content: `Apple will use autopilot chips built by a South Korean firm in its first
self-driving car, according to a new report.The two companies joined
             self-driving car, according to a new report.The two companies joined
             self-driving car, according to a new report.The two companies joined
             
              forces around a year ago and are said to be working on `,
        },
        {
          source: {
            id: null,
            name: "Cult of Mac",
          },
          author: "Killian Bell",
          title:
            "Google tasks South Korean firm with building autopilot chips for its first car",
          description: `Apple will use autopilot chips built by a South Korean firm in its first self-driving
             car, according to a new report. The two companies joined forces around a year ago and are 
            said to be working on a chipset package that is likely to include a CPU, GPU, memor…`,
          url: "https://www.cultofmac.com/767354/apple-car-autopilot-chips/",
          urlToImage:
            "https://cdn.cultofmac.com/wp-content/uploads/2021/12/vanamara-apple-car-concept4.jpg",
          publishedAt: "2022-02-22T14:08:15Z",
          content: `Apple will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on `,
        },
        {
          source: {
            id: null,
            name: "Cult of Mac",
          },
          author: "Killian Bell",
          title:
            "Microsoft tasks South Korean firm with building autopilot chips for its first car",
          description: `Apple will use autopilot chips built by a South Korean firm in its first self-driving
             car, according to a new report. The two companies joined forces around a year ago and are 
            said to be working on a chipset package that is likely to include a CPU, GPU, memor…`,
          url: "https://www.cultofmac.com/767354/apple-car-autopilot-chips/",
          urlToImage:
            "https://cdn.cultofmac.com/wp-content/uploads/2021/12/vanamara-apple-car-concept4.jpg",
          publishedAt: "2022-02-22T14:08:15Z",
          content: `Henok will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on 
              Apple will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on 
              Apple will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on 
              Apple will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on `,
        },
        {
          source: {
            id: null,
            name: "Cult of Mac",
          },
          author: "Killian Bell",
          title:
            "Amazon tasks South Korean firm with building autopilot chips for its first car",
          description: `Apple will use autopilot chips built by a South Korean firm in its first self-driving
             car, according to a new report. The two companies joined forces around a year ago and are 
            said to be working on a chipset package that is likely to include a CPU, GPU, memor…`,
          url: "https://www.cultofmac.com/767354/apple-car-autopilot-chips/",
          urlToImage:
            "https://cdn.cultofmac.com/wp-content/uploads/2021/12/vanamara-apple-car-concept4.jpg",
          publishedAt: "2022-02-22T14:08:15Z",
          content: `Apple will use autopilot chips built by a South Korean firm in its first
             self-driving car, according to a new report.\r\nThe two companies joined
              forces around a year ago and are said to be working on `,
        },
      ],
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