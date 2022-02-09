<template>
  <div class="working container">
    <div class="heading">
      <h2>Working <em>process</em></h2>
    </div>
    <div class="cards">
      <WorkingCard v-for="(elem, index) in cards" :key="index" :card="elem" />
    </div>
    <img class="line" src="../../assets/illustration/svg/svg-3.svg" />
  </div>
</template>

<script>
import WorkingCard from "../common/WorkingCard.vue";

export default {
  name: "Working",

  components: {
    WorkingCard,
  },

  data() {
    return {
      cards: [
        {
          icon: "fa-solid fa-lightbulb",
          text: "Lorem ipsum dolor sit, conetu adipisc sed be et are aliqua pleasure itself",
          color: "green",
        },
        {
          icon: "fa-solid fa-comment",
          text: "Lorem ipsum dolor sit, conetu adipisc sed be et are aliqua pleasure itself",
          color: "yellow",
        },
        {
          icon: "fa-solid fa-cloud",
          text: "Lorem ipsum dolor sit, conetu adipisc sed be et are aliqua pleasure itself",
          color: "purple",
        },
        {
          icon: "fa-solid fa-pen",
          text: "Lorem ipsum dolor sit, conetu adipisc sed be et are aliqua pleasure itself",
          color: "red",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";

.working {
  padding: 120px 0px;
  position: relative;

  .heading {
    margin-bottom: 60px;
    text-align: center;
  }
}

.cards {
  @include display-flex(center);
  flex-wrap: wrap;
}

.line {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 1000px;
}
</style>
