<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterMiddle from "./components/AppFooterMiddle.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";
import AppCard from "./components/AppCard.vue";
import AppJumbotron from "./components/AppJumbotron.vue";
import DCComics from "../src/dc-comics.json"

export default {

  data() {
    return {
      DCComics
    };
  },

  components: {
    AppHeader,
    AppCard,
    AppJumbotron,
    AppFooterTop,
    AppFooterMiddle,
    AppFooterBottom,
  },
};
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <AppJumbotron />

  <AppCard :comics="DCComics" />

  <footer>
    <AppFooterTop />

    <AppFooterMiddle />

    <AppFooterBottom />
  </footer>
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
