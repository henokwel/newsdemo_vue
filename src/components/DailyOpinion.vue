<template>
  <div id="opinionContainer">
    <div id="opinionContainer">
      <div v-for="(post, index) in article" :key="index">
        <ArticleCard  :item="post" :mediaCard="true" />
      </div>
    </div>
  </div>
</template>



<script>
import ArticleCard from './ArticleCard.vue';
export default {
  components: { ArticleCard },
  data() {
    return {
      article: [
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
#opinionContainer {
  grid-area: opinion;
  /* background: paleturquoise; */
  /* border: 2px solid; */
  margin-left: 10px;
}
</style>