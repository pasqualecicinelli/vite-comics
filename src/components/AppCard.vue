<script>
export default {
  data() {
    return {
      cardsDC: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="container-card">
      <div class="button-blu">CURRENT SERIES</div>

      <div v-for="card in cardsDC" class="card">
        <img :src="card.thumb" alt="" />
        <span>{{ card.series.toUpperCase() }}</span>
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
    margin: 3rem 0;
    width: $width-standard;
    height: 500px;
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
      left: 15px;
    }

    .card {
      width: 180px;
      height: 220px;

      img {
        width: 180px;
        aspect-ratio: 1;
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
      margin-top: 3rem;
      background-color: $blu-light;
      color: $bg-header-text;
      font-size: 0.8rem;
      font-weight: bold;
    }
  }
}
</style>
