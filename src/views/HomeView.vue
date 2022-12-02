<template>
  <div class="home-view">
    <div class="background">
      <img class="mobile" src="/src/assets/images/mobile_bg.webp" />
      <img class="desktop" src="/src/assets/images/desktop_bg.webp" />
    </div>
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

.mobile {
  position: absolute;
  height: 100vh;
  top: 0;
  bottom: 0;
  right: 0;
  z-index: -1;
  filter: contrast(70%);
}

.desktop {
  display: none;
  position: absolute;
  height: 100vh;
  top: 0;
  bottom: 0;
  right: 0;
  z-index: -1;
  filter: contrast(70%);
}

.text_area {
  margin: 0 auto;
}

@media (min-width: 1000px) {
  .mobile {
    display: none;
  }

  .desktop {
    display: block;
  }
}
</style>
