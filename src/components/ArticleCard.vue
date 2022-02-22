<template>
  <!-- Title -->
  <!-- Content -->
  <!-- Author -->
  <!-- Time to read -->
  <div id="articleContainer">
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
      <span>{{this.readingTime}}m read</span>
    </div>
  </div>
</template>


<script>
//  If its textOnly render without media
export default {
  props: {
    textOnly: Boolean,
    item: Object,
  },

  computed: {
    readingTime() {
      const text = this.item.content;
      const wpm = 120;
      const words = text.trim().split(/\s+/).length;
      const time = Math.ceil(words / wpm);
      console.log(text);
      
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
  color: #6e6e6e;
  /* background: red; */
}
</style>