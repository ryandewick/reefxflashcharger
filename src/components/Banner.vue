<template>
  <div class="banner">
    <div class="banner_img">
      <img src="/src/assets/images/reef.png" alt="reef logo" />
    </div>
    <div>
      <img src="/src/assets/images/x.png" alt="image of an x" />
    </div>
    <div class="banner_img">
      <img src="/src/assets/images/flashcharger.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.banner {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px 0;
}

.banner_img img {
  width: 150px;
  margin: 0 10px;
}

@media (min-width: 800px) {
  .banner_img img {
    width: 200px;
    margin: 0 50px;
  }

  @media (min-width: 1280px) {
    .banner_img img {
      width: 250px;
    }
  }
}
</style>
