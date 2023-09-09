<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterMiddle from "./components/AppFooterMiddle.vue";

export default {
  data() {
    return {};
  },

  components: { AppHeader, AppFooterTop, AppFooterMiddle },
};
</script>

<template>
  
  <AppHeader />

  <h1>body center</h1>

  <AppFooterTop />

  <AppFooterMiddle />

</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
