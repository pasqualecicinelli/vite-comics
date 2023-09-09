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
  <footer>
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
  </footer>
</template>

<style lang="scss" scope>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

footer {

  @include center();
  height: 150px;
  background-color: $blu-light;
 
}

.top-footer {
  max-width: 1200px;
  

  .card-img-top {
    width: 50px;
    

    img {
      width: 60px;
      height: 50px;
      object-fit: contain;
    }
  }

  ul {
    display: flex;
    width: 100%;

    li {
      display: flex;
      width: 100%;
      align-items: center;
      margin: 0 10px;
      
      
    }

    a{
      margin: 0 20px;
      color:$bg-header-text;
    }
   
  }
}
</style>
