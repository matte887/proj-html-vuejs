<template>
  <div class="ms_header-container">
    <header>
      <div
        class="
          container
          d-flex
          justify-content-between
          align-items-center
          h-100
        "
      >
        <img
          class="ms_logo"
          src="../assets/images/Selected/logo-2x.png"
          alt=""
        />
        <nav class="d-flex align-items-center">
          <ul
            class="d-flex align-items-center justify-content-around flex-grow-1"
          >
            <li v-for="(item, index) in navItems" :key="index">
              <a href="">{{ item }}</a>
            </li>
          </ul>
          <a class="ms_dark-button me-5" href="">Join Us</a>
          <div class="ms_search">
            <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
          </div>
        </nav>
      </div>
    </header>
    <div class="ms_jumbotron">
        <div class="container">
            <h1>Jumbotron!</h1>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    navItems: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

header {
  width: 100%;
  height: $header-height;
  background-color: $brand-primary-color;
  color: $white-shade;
  .ms_logo {
    height: 60%;
  }
  nav {
    width: 70%;
    ul {
      margin-bottom: 0;
    }
  }
}

.ms_jumbotron {
    width: 100%;
    height: 60vh;
    background-image: url(../assets/images/Selected/home_slider_bg.jpg);
    background-repeat: no-repeat;
    background-position: center;
}
</style>