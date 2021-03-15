<template>
  
  <div class="container article-banner darker-bg">
    <div class="img-side">
      <img :src="require(`~/assets/article-${articles[focus].img_id}.jpg`)" alt="Article 1 - A violin">
      <ul class="dot-container">
        <template v-for="dotFocusId in 4">
          <li :key="dotFocusId - 1" class="dot-button shadow" :class="(dotFocusId - 1) == focus ? 'dot-focus' : ''" @click="chooseArticle(dotFocusId - 1)"></li>
        </template>
      </ul>
    </div>
    <div class="text-side">
      <h1>{{articles[focus].title.toUpperCase()}}</h1>
      <h2>{{articles[focus].desc}}</h2>
      <nuxt-link to="/" class="article-button btn">READ MORE</nuxt-link> <!-- Bind the articles[focus] id into the button url -->
    </div>
  </div>

</template>

<script>
import {articlesList} from "../localDatabase/globalData";

export default {
  name: "ArticleBanner",
  data() {
    return {
      articles: articlesList,
      focus: 0,
      focusChange: null
    }
  },
  mounted() {
    this.setFocusTimer();
  },
  methods: {
    chooseArticle(id) {
      this.focus = id;

      // Reset timer after user click, so it doesn't change too fast
      clearInterval(this.focusChange);
      this.setFocusTimer();
    },
    setFocusTimer() {
      this.focusChange = setInterval(
        () => {
          if(this.focus < 3){ this.focus += 1; } else { this.focus = 0; }
        }, 4000
      );
    }
  }
}
</script>

<style scoped>
.article-banner {
  position: relative;
  height: 400px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  overflow-y: hidden;
}

.dot-container {
  position: absolute;
  bottom: 1em;
  display: flex;
  width: 50%;
}

.dot-button {
  margin: 0 1em;
  width: 1em;
  height: 1em;
  border: 2px solid rgba(0, 0, 0, 0.9);
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.2);
}

.dot-button:hover {
  border: 1px solid rgba(0, 0, 0, 0.5);
  background-color: rgba(255, 255, 255, 0.95);
}

.dot-focus {
  border: 2px solid rgba(0, 0, 0, 0.9);
  background-color: rgba(255, 255, 255, 1);
}

.img-side {
  max-width: 50%;
}

.text-side {
  max-width: 50%;
  text-align: right;
  padding: 1em;
}

.text-side h1 {
  font-weight: 700;
  font-size: 1.75em;
  padding: 0.75em;
  background-color: rgba(0, 0, 0, 0.4);
}

.text-side h2 {
  padding: 0 1em;
  margin-top: 1em;
  font-size: 1em;
}

.article-button {
  position: absolute;
  bottom: 1.5em;
  right: 1.5em;
}

</style>
