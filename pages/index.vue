<template>
  <div>
    <ArticleBanner />
    <HomeNews />
    <PastConcerts />
  </div>
</template>

<script>
import ArticleBanner from "../components/ArticleBanner";
import HomeNews from "../components/HomeNews";
import PastConcerts from "../components/PastConcerts";

export default {
  components: {
    ArticleBanner,
    HomeNews,
    PastConcerts
  }
}
</script>

<style>

</style>
