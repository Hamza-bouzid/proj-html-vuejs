<template>
  <div class="card">
    <div class="card-icon" :class="card.color">
      <i :class="card.icon"></i>
    </div>
    <h5>Firs there an idea</h5>
    <p>Lorem ipsum dolor sit, conetu adipisc sed be et are aliqua pleasure itself</p>
  </div>
</template>

<script>
export default {
  name: "WorkingCard",

  props: {
    card: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/reusable.scss";
.card {
  width: 300px;
  text-align: center;
  @include display-flex(center);
  flex-direction: column;
  padding: 0px 10px;
  z-index: 100;

  &-icon {
    @include display-flex(center);
    background-color: #faf7f1;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    font-size: 35px;
  }

  h5 {
    font-size: 18px;
    font-weight: normal;
    margin: 10px 0px;
  }

  p {
    font-size: 13px;
  }
}

.green {
  color: #badac9;
}

.yellow {
  color: #f9d12c;
}

.purple {
  color: #80455f;
}

.red {
  color: #eb6950;
}
</style>
