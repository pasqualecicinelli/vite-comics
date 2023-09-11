<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterMiddle from "./components/AppFooterMiddle.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";
import AppCard from "./components/AppCard.vue";
import AppJumbotron from "./components/AppJumbotron.vue";

export default {
  data() {
    return {};
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

  <AppCard />

  <footer>
    <AppFooterTop />

    <AppFooterMiddle />

    <AppFooterBottom />
  </footer>
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
