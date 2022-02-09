<template>
  <div class="working container">
    <div class="heading">
      <h2>Working <em>process</em></h2>
    </div>

    <div class="cards">
      <WorkingCard />
    </div>
  </div>
</template>

<script>
import WorkingCard from "../common/WorkingCard.vue";

export default {
  name: "Working",

  components: {
    WorkingCard,
  },
};
</script>

<style lang="scss" scoped>
.working {
  padding: 100px 0px;
}
</style>
