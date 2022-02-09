<template>
  <div class="banner">
    <div class="container">
      <h2>Want to work whit us? Send us <em>a message!</em></h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor nam maxime, quasi doloremque cupiditate fugit, minus deleniti ab commodi voluptatum voluptas molestiae id accusamus assumenda</p>

      <a class="header-link" href="#">Contact</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";

.banner {
  padding: 100px 0px;
  background: url("../../assets/illustration/img/h-2-background-1.jpg") no-repeat;
  background-size: cover;
  @include display-flex(center);
  flex-direction: column;
  text-align: center;

  p {
    margin: 20px 0px 30px 0px;
  }

  a {
    padding: 10px 40px;
    transition: all 0.1s linear;
    background-color: #c0e1cf;

    &:hover {
      color: #fff;
      background-color: #e1c0b0;
    }
  }
}
</style>
