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
    <div class="container">
      <img src="img/dc-logo.png" alt="" />

      <div class="navbar">
        <ul>
          <li v-for="(link, index) in links">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header{
  width: 100%;
 background-color: $bg-header-text;
}

.container {
  @include beetwen();
  width: $width-standard;
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
