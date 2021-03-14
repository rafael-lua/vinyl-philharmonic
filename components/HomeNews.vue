<template>
  <div class="container news-area dark-bg">
    <template v-for="n in 4">
      <div class="news-banner shadow-light" :key="n">
        <div class="news-info">
          <h2>Title</h2>
          <h3>Description Etiam sed mauris in sapien scelerisque tristique. Quisque mollis dapibus pulvinar. Nullam posuere dapibus erat, eget pulvinar diam imperdiet ut. Nunc id mollis nunc.</h3>
        </div>
        <div class="news-date">
          <p>Date</p>
        </div>
      </div>
    </template>
  </div>
</template>

<script>
export default {
  name: "HomeNews"
}
</script>

<style>
.news-area {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 1em;
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
  font-size: 0.85em;
  word-wrap: break-word;
}

.news-banner .news-date {
  width: 75%;
  margin: 0 auto;
  text-align: center;
  padding: 0.25em;
 
}

.news-banner .news-date p {
  font-size: 0.85em;
  font-weight: 700;
  font-style: italic;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

</style>