<template>
  <footer>
    <ArrowBottom />
    <div class="container">
      <div class="footer">
        <div class="footer-logo">
          <a href="#"><img src="../assets/illustration/img/logo-sidearea-1.png" /></a>
          <span>Let's Get Creative</span>
        </div>
        <div class="footer-contacts">
          <div class="hb_margin-bottom">
            <a href="mailto:maree.qode@gmail.com">maree.qode@gmail.com</a>
          </div>
          <div>
            <a href="tel:+44645321789">+44645 321 789</a>
          </div>
        </div>
        <div class="footer-address">
          <a href="#">
            <span class="hb_margin-bottom">Avenue d'Auderghem 10</span>
            <span>1040 Brussels, Belgium</span>
          </a>
        </div>
        <div class="footer-social">
          <span class="hb_margin-bottom">Stay in touch with us</span>
          <div class="footer-socila_links">
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-pinterest-p"></i></a>
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import ArrowBottom from "./common/ArrowBottom.vue";
export default {
  name: "Footer",

  components: {
    ArrowBottom,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/reusable.scss";
footer {
  padding: 50px 0px;
  background-color: #c0e1cf;
  font-size: 12px;
  position: relative;
}

span {
  display: block;
}

.footer {
  @include display-flex(space-between);
  padding: 0px 50px;

  &-logo {
    img {
      width: 100px;
      margin-bottom: 5px;
    }
  }

  .footer-socila_links {
    @include display-flex(space-between);
    a {
      font-size: 15px;
    }
  }
}

.hb_margin-bottom {
  margin-bottom: 10px;
}
</style>
