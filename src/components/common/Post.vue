<template>
  <div class="post">
    <img :src="post.image" />
    <div class="post-text">
      <h4>{{ post.text }}</h4>
      <em>By {{ post.author }}</em>
    </div>
    <div class="post-date">
      <div class="post-date_number">
        <em>{{ post.postNumber }}</em>
      </div>
      <div class="post-date_day">
        <span>{{ post.date }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",

  props: {
    post: Object,
  },
};
</script>

<style lang="scss" scoped>
.post {
  width: 350px;
  margin: 0px 10px;
  position: relative;
  img {
    width: 100%;
    height: 100%;
  }

  &-text {
    padding: 10px 10px 10px 0px;

    h4 {
      margin: 5px 0px;
      font-size: 20px;
      font-weight: normal;
    }

    em {
      font-size: 11px;
      font-weight: 100;
    }
  }

  &-date {
    position: absolute;
    top: -10px;
    left: 10px;
    text-align: center;
    width: 60px;

    &_number {
      background-color: #c0e1cf;
      font-size: 24px;
    }

    &_day {
      background-color: #f3d0c7;
      padding-top: 3px;
      text-transform: uppercase;
      font-size: 12px;
      font-weight: 600;
      height: 30px;
      clip-path: polygon(100% 0, 100% 100%, 50% 78%, 0 100%, 0 0);
    }
  }
}
</style>
