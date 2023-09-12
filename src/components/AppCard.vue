<script>
export default {
  props: {
    comics: Array,
  },
};
</script>

<template>
  <main>
    <div class="container-card">
      <div class="button-blu">CURRENT SERIES</div>

      <div v-for="comic in comics" class="card">
        <img :src="comic.thumb" alt="" />
        <span>{{ comic.series.toUpperCase() }}</span>
      </div>

      <div class="button-blu-bottom">LOAD MORE</div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

main {
  @include center();
  width: 100%;
  background-color: $bg-body-text;

  .container-card {
    @include evenly();
    flex-wrap: wrap;
    margin: 3rem 0 1.5rem 0;
    width: $width-standard;
    height: 600px;
    position: relative;
    .button-blu {
      padding: 1rem;
      background-color: $blu-light;
      color: $bg-header-text;
      font-size: 1.25rem;
      font-weight: bold;
      position: absolute;
      z-index: 1;
      top: -70px;
      left: 0;
    }

    .card {
      width: 180px;
      height: 250px;

      img {
        width: 150px;
        height: 200px;
        object-fit: cover;
      }
      span {
        font-size: 0.75rem;
        color: $bg-header-text;
        margin-top: 1rem;
        display: block;
      }
    }

    .button-blu-bottom {
      padding: 0.8rem 3.5rem;
      margin-top: 4rem;
      background-color: $blu-light;
      color: $bg-header-text;
      font-size: 0.8rem;
      font-weight: bold;
    }
  }
}
</style>
