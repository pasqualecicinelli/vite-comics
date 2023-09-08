<script>
export default {
  data() {
    return {
      titleHead: "header",
    };
  },
};
</script>

<template>
  <header>
    <div class="container-header">
      <img src="img/dc-logo.png" alt="" />

      <navbar>
        <ul>
          <li><a href="#">1</a></li>
          <li><a href="#">2</a></li>
          <li><a href="#">3</a></li>
          <li><a href="#">4</a></li>
          <li><a href="#">5</a></li>
          <li><a href="#">6</a></li>
          <li><a href="#">7</a></li>
          <li><a href="#">8</a></li>
          <li><a href="#">9</a></li>
          <li><a href="#">10</a></li>
        </ul>
      </navbar>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;

header {
  border: 1px solid black;
}

.container-header {
  @include beetwen();

  max-width: 1000px;
  height: 100px;
  margin-left: auto;
  margin-right: auto;

  img {
    width: 8%;
  }

  ul {
    display: flex;
    list-style: none;
    li {
      margin: 10px;
      a {
        text-decoration: none;
      }
    }
  }
}
</style>
