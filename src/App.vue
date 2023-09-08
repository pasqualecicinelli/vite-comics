<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  data() {
    return {
      
    };
  },

  components: { AppHeader, AppFooter },

};
</script>

<template>

  <AppHeader />

  <h1>body center</h1>

  <AppFooter />

</template>

<style lang="scss">
@use './style/general.scss' as *;



</style>
