<template>
  <nav>
    <ul>
      <li>
        <a class="header-link" :href="link.url"
          >{{ link.name }}
          <div class="hover-active" :class="{ active: link.active }"></div>
        </a>
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

    a {
      position: relative;
      z-index: 100;
    }
  }

  .active {
    display: block !important;
  }

  .hover-active {
    background-color: #f5d8ca;
    height: 6px;
    width: 100%;
    position: absolute;
    bottom: 2px;
    z-index: -1;
    left: 0;
    display: none;
  }
}
</style>
