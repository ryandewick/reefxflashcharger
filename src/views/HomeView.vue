<template>
  <div class="home-view">
    <!-- <img src="/src/assets/images/mobile_bg.png" alt="" /> -->
    <Banner />
    <MainTextArea class="text_area" />
  </div>
</template>

<script>
import MainTextArea from "../components/MainTextArea.vue";
import Banner from "../components/Banner.vue";
export default {
  components: { MainTextArea, Banner },
};
</script>

<style scoped lang="scss">
.home-view {
  width: 100%;
  // position: relative;
}

// img {
//   position: absolute;
//   width: 120%;
//   aspect-ratio: 1;
//   // min-height: 100%;
//   // transform: scale(1.2);
//   top: 0;
//   right: 0;
// }

.text_area {
  margin: 0 auto;
}
</style>
