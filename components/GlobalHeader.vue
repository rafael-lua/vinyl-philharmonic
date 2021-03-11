<template lang="en">
  <header>
    Welcome! {{msg}}
    <hr>
  </header>
</template>

<script>
import {listOfThings} from "../localDatabase/globalData";

export default {
  name: "GlobalHeader",
  data() {
    return {
      msg: listOfThings.athing
    }
  }
}
</script>

<style lang="en">
  
</style>