<template>
  <div class="posts container">
    <Post v-for="(elem, index) in posts" :key="index" :post="elem" />
  </div>
</template>

<script>
import Post from "../common/Post.vue";

export default {
  name: "Posts",

  components: {
    Post,
  },

  data() {
    return {
      posts: [
        {
          image: require("../../assets/illustration/img/h-2-blog-img-1.jpg"),
          text: "This way, loves: a detailed guide trhough new design",
          author: "Emily Fileds",
        },
        {
          image: require("../../assets/illustration/img/h-2-blog-img-2.jpg"),
          text: "I try to give people a different way of loking art",
          author: "Emily Fileds",
        },
        {
          image: require("../../assets/illustration/img/h-2-blog-img-3.jpg"),
          text: "Introduce Richard Laperrière of those amazing features",
          author: "Emily Fileds",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";
.posts {
  padding: 120px 0px;
  @include display-flex(center);
  flex-wrap: wrap;
}
</style>
