<template>
  <div class="content-post">
    <div class="arrow">
      <div class="posts container">
        <ArrowTop />
        <Post v-for="(elem, index) in posts" :key="index" :post="elem" />
      </div>
    </div>
  </div>
</template>

<script>
import Post from "../common/Post.vue";
import ArrowTop from "../common/ArrowTop.vue";

export default {
  name: "Posts",

  components: {
    Post,
    ArrowTop,
  },

  data() {
    return {
      posts: [
        {
          image: require("../../assets/illustration/img/h-2-blog-img-1.jpg"),
          text: "This way, loves: a detailed guide trhough new design",
          author: "Emily Fileds",
          postNumber: "07",
          date: "May '19",
        },
        {
          image: require("../../assets/illustration/img/h-2-blog-img-2.jpg"),
          text: "I try to give people a different way of loking art",
          author: "Emily Fileds",
          postNumber: "07",
          date: "May '19",
        },
        {
          image: require("../../assets/illustration/img/h-2-blog-img-3.jpg"),
          text: "Introduce Richard Laperrière of those amazing features",
          author: "Emily Fileds",
          postNumber: "07",
          date: "May '19",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";
.content-post {
  padding: 30px 0px;
}
.arrow {
  position: relative;
}
.posts {
  padding: 100px 0px;
  @include display-flex(center);
  flex-wrap: wrap;
}
</style>
