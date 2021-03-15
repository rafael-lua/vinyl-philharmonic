<template>
  <div class="container news-area dark-bg">
    <h1 class="section-title">NEWS</h1>
    <hr class="section-hr">
    <div class="news-wrapper">
      <template v-for="newsId in 4">

        <nuxt-link to="/" :key="newsId"> <!-- Add the link to the news based on their id -->

          <div class="news-banner shadow">
            <div class="news-info">
              <h2>{{newsList[newsId - 1].title}}</h2>
              <h3>{{newsList[newsId - 1].desc}}</h3>
            </div>
            <div class="news-date">
              <p>{{newsList[newsId - 1].date}}</p>
            </div>
          </div>

        </nuxt-link>

      </template>
    </div>
  </div>
</template>

<script>
import {newsList} from "../localDatabase/globalData";

export default {
  name: "HomeNews",
  data() {
    return {
      newsList: newsList
    }
  }
}
</script>

<style scoped>
.news-area {
  padding: 1em;
}

.news-wrapper {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.news-banner {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 0.75em;
  height: 200px;
  width: 250px;
  background-color: var(--primary-color);
}

.news-info {
  max-width: 100%;
}

.news-info h2 {
  font-weight: 700;
  font-size: 1em;
  margin: 0.75em 0 1em 0;
}

.news-info h3 {
  height: 75px;
  font-size: 0.85em;
  word-wrap: break-word;
}

.news-date {
  width: 75%;
  margin: 0 auto;
  text-align: center;
  padding: 0.25em;
 
}

.news-date p {
  font-size: 0.85em;
  font-weight: 700;
  font-style: italic;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.news-banner:hover {
  color: var(--link-color) !important;
  border: 1px solid var(--link-color);
}

</style>