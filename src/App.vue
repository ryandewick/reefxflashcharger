<script>
import HomeView from "./views/HomeView.vue";

export default {
  name: "App",
  metaInfo: {
    title: "Free charging for all Reef customers",
    titleTemplate: "%s | Reef x Flashcharger",
    htmlAttrs: {
      lang: "en-GB",
    },
    meta: [
      { charset: "utf-8" },
      {
        name: "description",
        content:
          "A collaboration between Reef and Flashcharger which offers all Reef customers free charging!",
      },
      { name: "viewport", content: "width=device-width, initial-scale=1" },
    ],
  },
};
</script>

<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style></style>
