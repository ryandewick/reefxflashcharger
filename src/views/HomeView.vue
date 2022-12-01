<template>
  <div class="home-view">
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
}

.text_area {
  margin: 0 auto;
}
</style>
