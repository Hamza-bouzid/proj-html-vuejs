<template>
  <div class="container">
    <div class="jumbo">
      <div class="jumbo-heading">
        <h1>Devotion that never<em class="text-bold">ends</em></h1>

        <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.</p>

        <a class="header-link" href="#">Read More</a>
      </div>
      <div class="jumbo-image">
        <div class="big-image">
          <img src="../../assets\illustration\img\h-2-slider-img-15.png" />
          <img src="../../assets\illustration\img\h-2-slider-img-16.png" />
        </div>

        <!--Small Images-->
        <img src="../../assets\illustration\img\short-slider-rev-1-img-2.png" class="small-image small-image-1" />
        <img src="../../assets\illustration\img\h-2-slider-img-12.png" class="small-image small-image-2" />
        <img src="../../assets\illustration\img\h-2-slider-img-13.png" class="small-image small-image-3" />
        <img src="../../assets\illustration\img\h-2-slider-img-14.png" class="small-image small-image-4" />
        <img src="../../assets\illustration\img\short-slider-rev-1-img-6.png" class="small-image small-image-5" />
        <img src="../../assets\illustration\img\h-2-slider-img-17.png" class="small-image small-image-6" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbo",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";

.jumbo {
  padding: 100px 0px;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;

  &-heading {
    width: 50%;
    h1 {
      font-size: 60px;
      font-weight: 400;
      line-height: 70px;
    }

    p {
      color: #878787;
      margin: 20px 0px 40px 0px;
    }

    .text-bold {
      font-family: "Domine", serif;
      font-weight: bold;
    }

    a {
      padding: 12px 30px;
      border: 3px solid #e1c0b0;
      transition: all 0.1s linear;

      &:hover {
        color: #fff;
        background-color: #e1c0b0;
      }
    }
  }

  &-image {
    @include display-flex(center);
    position: relative;

    .big-image {
      img {
        width: 250px;
        height: 320px;
      }
    }

    .small-image {
      width: 35px;
      position: absolute;
    }
    .small-image-1 {
      top: -30px;
      left: 0px;
    }
    .small-image-2 {
      top: 50%;
      left: -70px;
    }
    .small-image-3 {
      bottom: 0;
      left: -50px;
    }
    .small-image-4 {
      top: -50px;
      right: 20px;
    }
    .small-image-5 {
      top: 50px;
      right: -20px;
    }
    .small-image-6 {
      bottom: 0;
      right: -50px;
      width: 55px;
    }
  }
}
</style>
