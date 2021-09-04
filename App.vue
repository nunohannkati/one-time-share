<template>
  <div id="app">
    <Header />
    <div class="twoColumnContainer">
      <Slider />
      <Twitter />
    </div>
    <Broadcast />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Slider from "./components/Slider.vue";
import Twitter from "./components/Twitter.vue";
import Broadcast from "./components/Broadcast.vue";

export default {
  name: "App",
  components: {
    Header,
    Slider,
    Twitter,
    Broadcast,
  },
};
</script>

<style>
body {
  font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic, "游ゴシック体",
    "ヒラギノ角ゴ Pro W3", sans-serif;
  line-height: 1.7;
  color: #432;
  margin: 0;
}

.twoColumnContainer {
    display: grid;
    grid-template-rows: 1fr;
    grid-template-columns: 1fr 350px;
    gap: 0px;
    padding-top: 0px;
    margin: 0px 0px 0px 0px;
}
</style>
