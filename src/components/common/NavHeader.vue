<template>
  <nav>
    <ul>
      <li>
        <a class="header-link" :class="{ active: link.active }" :href="link.url">{{ link.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavHeader",

  props: {
    link: Object,
  },
};
</script>

<style lang="scss" scoped>
nav {
  ul li {
    display: inline-block;
    margin: 0px 20px;
  }

  .active {
    background-color: #e1c0b0;
    height: 50%;
  }
}
</style>
