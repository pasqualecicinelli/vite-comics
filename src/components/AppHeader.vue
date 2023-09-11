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

      activeLink: 0,
    };
  },

  methods: {
    clickLink(index) {
      this.activeLink = index;
    },
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="img/dc-logo.png" alt="" />

      <nav>
        <ul>
          <li v-for="(link, index) in links">
            <a
              class="navLinks"
              :class="index == activeLink ? 'active' : ''"
              @click="clickLink(index)"
              href="#"
              >{{ link }}</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
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
    width: 70px;
  }

  ul {
    display: flex;
    li {
      margin: 10px;
      a {
        font-size: 0.75rem;
        font-weight: bold;
        color: $header-text;
      }
      .navLinks.active {
        color: $blu-light;
        //aggiungere hover
      }
    }
  }
}
</style>
