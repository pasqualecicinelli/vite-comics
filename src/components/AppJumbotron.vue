<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
<div class="jumbotron"></div>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.jumbotron {
    position: relative;
    width: 100%;
    height: 400px;
    background-image: url("../../img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>