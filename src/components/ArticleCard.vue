<template>
  <!-- Title -->
  <!-- Content -->
  <!-- Author -->
  <!-- Time to read -->
  <div
    id="articleContainer"
    :class="{ mediaContainer: mediaCard, miniCardContainer: miniCard }"
  >
    <div id="articleMedia" v-show="mediaCard || miniMedia">
      <img :src="item.urlToImage" alt="Img" />
    </div>
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <h3 id="title">
      <router-link id="navLink" to="/">
        {{ item.title }}
      </router-link>
    </h3>
    <p id="content">
      {{ item.content }}
    </p>
    <div id="articleAuthor">
      <span>{{ item.author }}</span>
      <span>{{ this.readingTime }}m read</span>
    </div>
  </div>
</template>


<script>
//  If its textOnly render without media
export default {
  props: {
    item: Object,
    mediaCard: {
      type: Boolean,
      default: false,
    },
    miniCard: {
      type: Boolean,
      default: false,
    },
    miniMedia: {
      type: Boolean,
      default: false,
    },
  },

  computed: {
    readingTime() {
      const text = this.item.content;
      const wpm = 120;
      const words = text.trim().split(/\s+/).length;
      const time = Math.ceil(words / wpm);

      return time;
    },
  },
};
</script>



<style scoped>
#articleContainer {
  max-width: 400px;
  min-height: 250px;
  word-wrap: break-word;
  text-align: left;
  border-bottom: 1px solid #bcbcbc;
  margin-bottom: 10px;
}

#articleMedia img {
  width: 100%;
}

#title a {
  text-decoration: none;
  color: black;
}

#content {
  max-height: 90px;
  overflow: hidden;
  word-wrap: break-word;
  text-overflow: ellipsis;
  /* background: greenyellow; */
  font-family: "Open Sans", sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 15px;
  line-height: 150%;
  /* or 22px */
  letter-spacing: 0.02em;
}

#articleAuthor {
  padding: 5px;
  display: flex;
  justify-content: space-between;
  color: #858585;
  /* background: red; */
}

/* Article with any media content */
.mediaContainer {
  min-width: 80%;
  
    /* min-height: 450px; */
  /* background: red; */
}

.mediaContainer #title {
  font-family: Inter;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 135%;
}

.mediaContainer #content {
  /* font-style: normal; */
  /* font-weight: normal; */
  font-size: 15px;
  /* line-height: 150%; */
  /* or 19px */

  letter-spacing: 0.02em;
}
 

.mediaContainer #articleAuthor{
  margin-bottom: 30px;
}

/* Articles with smaller content */

.miniCardContainer{
  /* background: rgb(99, 66, 72); */
  width: 330px;
  margin: 10px;
}
</style>