<template>
  <div class="ms_header-container">
    <!-- HEADER -->
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
        <!-- header logo -->
        <img
          class="ms_logo"
          src="../assets/images/selected/logo-2x.png"
          alt="Avada logo"
        />
        <!-- header logo -->

        <!-- header nav -->
        <nav class="d-flex align-items-center">
          <ul
            class="d-flex align-items-center justify-content-around flex-grow-1"
          >
            <li
              v-for="(item, index) in navItems"
              :key="index"
              @click="$emit('clickEvent', index)"
            >
              <a>{{ item.title }}</a>
              <!-- icona active -->
              <div
                :class="item.active ? 'ms_selected' : 'd-none'"
              ></div>
              <!-- /icona active -->

            </li>
          </ul>
          <a class="ms_btn ms_dark-btn me-5" href="">Join Us</a>
          <div class="ms_search">
            <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
          </div>
        </nav>
        <!-- /header nav -->
      </div>
    </header>
    <!-- /HEADER -->

    <!-- JUMBOTRON -->
    <div class="ms_jumbotron d-flex align-items-center">
      <div class="container">
        <h1>Tech Forum!</h1>
        <h3 class="mb-5">Discuss all the latest technology news and trends</h3>
        <a class="ms_btn ms_primary-btn" href="">
          Get Avada Now!
          <i class="fa-solid fa-angle-right"></i>
        </a>
      </div>
    </div>
    <!-- /JUMBOTRON -->
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
.ms_header-container {
  color: $white-shade;
  header {
    width: 100%;
    height: $header-height;
    background-color: $brand-primary-color;
    color: $white-shade;
    .ms_logo {
      height: 60%;
      width: auto;
    }
    nav {
      width: 70%;
      ul {
        margin-bottom: 0;
        .ms_selected {
          width: 0;
          height: 0;
          border-left: 12px solid transparent;
          border-right: 12px solid transparent;
          border-top: 13px solid $brand-primary-color;
          position: absolute;
          left: 38.5px;
          transform: translate(-50%, -50%);
          top: 68px;
        }
        
        li {
          position: relative;
          width: 77px;
          text-align: center;
        }
      }
    }
  }

  .ms_jumbotron {
    width: 100%;
    height: $jumbo-height;
    background-image: url(../assets/images/selected/home_slider_bg.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    h1 {
      font-size: 8rem;
      font-weight: 700;
    }
    h3 {
      font-weight: 400;
    }
  }
}

</style>