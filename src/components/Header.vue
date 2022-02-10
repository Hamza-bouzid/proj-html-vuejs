<template>
  <header id="Home">
    <div class="navigation">
      <div class="logo">
        <a href="#"><img src="../assets/illustration/img/logo-sidearea-1.png" /></a>
      </div>
      <div class="nav">
        <NavHeader v-for="(element, index) in menu" :key="index" :link="element" :counter="counter" @click.native="changeActive(element.id)" />
        <img src="../assets/illustration/svg/svg-1.svg" />
      </div>
    </div>
    <div class="container-large">
      <Jumbo />
    </div>
  </header>
</template>

<script>
import NavHeader from "./common/NavHeader.vue";
import Jumbo from "./section/Jumbo.vue";
export default {
  name: "Header",

  components: {
    NavHeader,
    Jumbo,
  },

  data() {
    return {
      counter: 1,
      menu: [
        {
          name: "Home",
          url: "#",
          active: true,
          id: 1,
        },
        {
          name: "Pages",
          url: "#",
          active: false,
          id: 2,
        },
        {
          name: "Portfolio",
          url: "#",
          active: false,
          id: 3,
        },
        {
          name: "Blog",
          url: "#",
          active: false,
          id: 4,
        },
        {
          name: "Shop",
          url: "#",
          active: false,
          id: 5,
        },
        {
          name: "Elements",
          url: "#",
          active: false,
          id: 6,
        },
      ],
    };
  },

  methods: {
    changeActive: function (input) {
      this.counter = input;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/reusable.scss";

header {
  padding: 15px 20px;

  .navigation {
    @include display-flex(space-between);

    .logo {
      img {
        width: 100px;
      }
    }
  }

  .nav {
    @include display-flex(center);
    img {
      width: 18px;
      margin-left: 20px;
    }
  }
}
</style>
