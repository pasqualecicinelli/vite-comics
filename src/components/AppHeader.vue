<script>
export default {
  data() {
    return {
      links: [
        "CHARACTERS",
        "COMICS",
        "MOVIES",
        "TV",
        "GAMES",
        "COLLECTIBLES",
        "VIDEOS",
        "FANS",
        "NEWS",
        "SHOP",
      ],
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
          <li v-for="(link, index) in links">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </navbar>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
  border: 1px solid black;
}

.container-header {
  @include beetwen();

  max-width: 1200px;
  height: 100px;
  margin-left: auto;
  margin-right: auto;

  img {
    width: 6%;
  }

  ul {
    display: flex;
    li {
      margin: 10px;
      a {
        font-size: 0.75rem;
        font-weight: bold;
        color:$header-text;
      }
    }
  }
}
</style>
