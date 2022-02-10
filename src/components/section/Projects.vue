<template>
  <div class="projects container-large">
    <!--Project 1-->
    <div id="card-1" class="projects-image">
      <img src="../../assets/illustration/img/h-2-port-img-1.jpg" />
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
    <!--Project 2-->
    <div id="card-2" class="projects-image">
      <img src="../../assets/illustration/img/h-2-port-img-2.jpg" />
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
    <!--Project 3-->
    <div id="card-3" class="projects-image small-image">
      <img src="../../assets/illustration/img/h-2-port-img-3.jpg" />
      <div class="icons">
        <a href="#"><img class="circle" src="../../assets/illustration/svg/svg-7.svg" /></a>
        <a href="#"><img class="carello" src="../../assets/illustration/svg/svg-6.svg" /></a>
      </div>
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
    <!--Project 4-->
    <div id="card-4" class="projects-image">
      <img src="../../assets/illustration/img/h-2-port-img-4.jpg" />
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
    <!--Project 5-->
    <div id="card-5" class="projects-image">
      <img src="../../assets/illustration/img/h-2-port-img-5.jpg" />
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
    <!--Project 6-->
    <div id="card-6" class="projects-image small-image-arrow">
      <img src="../../assets/illustration/img/h-2-port-img-6.jpg" />
      <ArrowBottom />
      <ArrowTop />
      <div class="placeholder">
        <h3>Illustrations of novels</h3>
        <em>Illustration</em>
      </div>
    </div>
  </div>
</template>

<script>
import ArrowBottom from "../common/ArrowBottom.vue";
import ArrowTop from "../common/ArrowTop.vue";

export default {
  name: "Projects",

  components: {
    ArrowBottom,
    ArrowTop,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";

.projects {
  @include display-flex(center);
  flex-wrap: wrap;

  &-image {
    width: 33.3%;
    height: auto;
    flex-grow: 1;
    margin: -5px 0px;
    position: relative;
    overflow: hidden;

    img {
      width: 100%;
      height: 100%;
    }
  }

  .placeholder {
    width: 250px;
    height: 80px;
    background-color: #fff;
    padding: 15px 20px;
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-50%);
    display: none;

    h3 {
      font-weight: 500;
    }

    em {
      font-size: 14px;
    }
  }
}

.small-image {
  position: relative;
  .icons {
    position: absolute;
    top: 90px;
    right: 0;
    display: flex;
    flex-direction: column;

    img {
      width: 30px;
    }

    .circle {
      background-color: #ee2852;
      padding: 8px;
    }

    .carello {
      background-color: #fff;
      color: #ee2852;
      padding: 8px;
    }
  }
}

.small-image-arrow {
  position: relative;
}

#card-1:hover .placeholder,
#card-2:hover .placeholder,
#card-3:hover .placeholder,
#card-4:hover .placeholder,
#card-5:hover .placeholder,
#card-6:hover .placeholder {
  display: block;
  animation: from-left 0.4s ease-out;
}

@keyframes from-left {
  0% {
    transform: translateX(-250px) translateY(-50%);
  }

  100% {
    transform: translateX(0px) translateY(-50%);
  }
}
</style>
