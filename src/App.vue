<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterMiddle from "./components/AppFooterMiddle.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";

export default {
  data() {
    return {};
  },

  components: { AppHeader, AppFooterTop, AppFooterMiddle, AppFooterBottom },
};
</script>

<template>
  
  <header>
    <AppHeader />
  </header>

  <h1>body center</h1>

  <footer>
    <AppFooterTop />

    <AppFooterMiddle />

    <AppFooterBottom />
  </footer>
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
