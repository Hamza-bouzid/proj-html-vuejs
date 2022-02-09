<template>
  <main>
    <Projects />
    <Working />
    <Banner />
    <Posts />
  </main>
</template>

<script>
import Projects from "./section/Projects.vue";
import Working from "./section/Working.vue";
import Banner from "./section/Banner.vue";
import Posts from "./section/Posts.vue";
export default {
  name: "Main",

  components: {
    Projects,
    Working,
    Banner,
    Posts
  },
};
</script>

<style lang="scss" scoped></style>
