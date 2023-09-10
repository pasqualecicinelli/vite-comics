<script>
export default {
  data() {
    return {
      links: [
        {
          title: "DC COMICS",
          lists: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "SHOP",
          lists: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          lists: [
            "Terms Of Use",
            "Privacy policy(New)",
            "Ad Chois",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certicates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          lists: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
      activeLink: 0,
    };
  },
};
</script>

<template>
  <div class="container-foot-middle">
    <div class="foot-middle">
      <ul>
        <li v-for="(link, index) in links">
          <a class="links-title" href="#">{{ link.title }} </a>

          <div v-for="list in links[index].lists">
            <a href="#">{{ list }}</a>
          </div>
        </li>
      </ul>

      <div class="img-dc">
        <img src="../../img/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.container-foot-middle {
  @include center();
  width: 100%;
  height: 370px;
  background-image: url(../../img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;

  .foot-middle {
    @include beetwen();
    width: $width-standard;
    height: 100%;

    ul {
      width: 45%;
      height: 80%;
      display: flex;

      li {
        margin-right: 20px;
        a.links-title {
          color: $bg-header-text;
          font-size: 1.25rem;
          margin-bottom: 15px;
          display: inline-block;
        }

        div {
          margin-bottom: 5px;

          a {
            color: $text-grey;
            font-size: 0.8rem;
          }
        }
      }
    }
    
  }
}
</style>
