<template>
  <div class="container concert-area darker-bg">
    <h1 class="section-title">PAST CONCERTS</h1>
    <hr class="section-hr">
    <div class="concert-wrapper">
      <template v-for="conId in 2">
        <nuxt-link to="/" :key="conId">
          <div class="concert-frame dark-bg shadow" @mouseover="concertHover = true; concertId = conId"
        @mouseleave="concertHover = false; concertId = 0">
            <img :src="require(`~/assets/concert-${concertList[conId - 1].img_id}.jpg`)" alt="Live concert photo">
            <h1 class="concert-title text-shadow">{{concertList[conId - 1].title}}</h1>
            <h3 v-if="concertId != conId" class="concert-date-check">{{concertList[conId - 1].date}}</h3>
            <h3 v-if="concertHover && concertId == conId" class="concert-date-check">CHECK IT OUT</h3>
          </div>
        </nuxt-link>
      </template>
    </div>
  </div>
</template>

<script>
import {concertList} from "../localDatabase/globalData";

export default {
  name: "PastConcerts",
  data() {
    return {
      concertList: concertList,
      concertHover: false,
      concertId: 0
    }
  }
}
</script>

<style scoped>
.concert-area {
  padding: 1em;
  height: 500px;
}

.concert-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.concert-frame {
  position: relative;
  margin: 0 2.5em;
  height: 350px;
  overflow: hidden;
}

.concert-frame:hover {
  border: 2px solid var(--link-color);
}

.concert-title {
  position: absolute;
  top: 0;
  text-align: center;
  width: 100%;
  font-size: 2em;
  font-weight: 700;
  word-wrap: break-word;
  padding: 0.5em;
  background-color: rgba(0, 0, 0, 0.25);
}

.concert-date-check {
  position: absolute;
  bottom: 0;
  text-align: center;
  width: 100%;
  font-size: 1.25em;
  font-weight: 700;
  font-style: italic;
  padding: 0.1em;
  background-color: rgba(0, 0, 0, 0.75);
}

</style>