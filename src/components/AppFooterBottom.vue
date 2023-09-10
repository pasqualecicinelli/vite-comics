<script>
export default {
  data() {
    return {
      icons: [
        "footer-facebook.png",
        "footer-twitter.png",
        "footer-youtube.png",
        "footer-pinterest.png",
        "footer-periscope.png",
      ],
    };
  },

  methods: {
    getIconsPath(nameIcon) {
      const iconUrl = new URL("../../img/" + nameIcon, import.meta.url);

      return iconUrl.href;
    },
  },
};
</script>

<template>
  <div class="container-foot-bottom">
    <div class="container">
      <div class="button">SIGN-UP NOW!</div>

      <div class="container-icons">
        <h3>FOLLOW US</h3>
        <ul>
          <li v-for="icon in icons">
            <a href="#"><img :src="getIconsPath(icon)" alt="" /></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scope>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.container-foot-bottom {
  width: 100%;
  height: 100px;
  background-color: $footer-bottom;
  position: relative;
  @include center();

  .container {
    @include beetwen();
    width: $width-standard;
    position: absolute;
    z-index: 0;

    .button {
      padding: 1rem;
      border: 1px solid $blu-light;
      color: $bg-header-text;
    }

    .container-icons {
      display: flex;
      align-items: center;

      h3 {
        color: $blu-light;
      }

      ul {
        display: flex;
        gap: 0.75em;
      }
    }
  }
}
</style>
