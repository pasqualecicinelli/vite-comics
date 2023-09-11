<script>
export default {
  data() {
    return {
      linksTopFoot: [
        {
          image: "buy-comics-digital-comics.png",
          description: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          description: "DC MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          description: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          description: "COMIC SHOP LOCAL",
        },
        {
          image: "buy-dc-power-visa.svg",
          description: "DC POWER VISA",
        },
      ],
      activeLink: 0,
    };
  },

  methods: {
    getImgPath(nameImage) {
      const imgUrl = new URL("../../img/" + nameImage, import.meta.url);

      return imgUrl.href;
    },
  },
};
</script>

<template>
  <div class="container-foot-top">
    <div class="top-footer">
      <ul>
        <li v-for="(link, index) in linksTopFoot">
          <div class="card-img-top">
            <img :src="getImgPath(link.image)" alt="" />
          </div>
          <a href="#">{{ link.description }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.container-foot-top {
  @include evenly();
  height: 150px;
  background-color: $blu-light;
  position: relative;
}

.top-footer {
  width: 1150px;
  position: absolute;
  z-index: 1;

  .card-img-top {
    width: 60px;

    img {
      width: 60px;
      height: 50px;
      object-fit: contain;
    }
  }

  ul {
    display: flex;
    width: 100%;
    padding: 0;
    gap: 2rem;

    li {
      display: flex;
      width: 100%;
      align-items: center;
      gap: 0.5rem;
    }

    a {
      font-size: 0.75rem;
      color: $bg-header-text;
    }
  }
}
</style>
