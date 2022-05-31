<template>
  <div id="app">
    <!-- header + jumbotron -->
    <AppHeader :navItems="headerMenu" @clickEvent="changeActive" />
    <!-- /header + jumbotron -->

    <!-- Main -->
    <AppMain />
    <!-- /Main -->

    <!-- Footer -->
    <AppFooter :footerItems="footerMenu" />
    <!-- /Footer -->

    <a href="#app" class="ms_back-to-top">
      <i class="fas fa-angle-up"></i>
    </a>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data() {
    return {
      // Vecchia versione
      // headerMenu: ['Home', 'Apple', 'Microsoft', 'Android', 'Forums', 'Contact us'],

      headerMenu: [
        {
          title: "Home",
          active: true,
        },
        {
          title: "Apple",
          active: false,
        },
        {
          title: "Microsoft",
          active: false,
        },
        {
          title: "Android",
          active: false,
        },
        {
          title: "Forums",
          active: false,
        },
        {
          title: "Contact us",
          active: false,
        },
      ],
      footerMenu: [
        {
          title: "Popular topics",
          voices: [
            "Morbi id velit fermentum, faucibus mauris ac, condimentum magna.",
            "Ut nec ante quis ex fermentum iaculis vel id orci.",
            "Nullam in mi eu augue egestas congue ut ac sem.",
            "Donec mollis nisi ac aliquet finibus.",
          ],
        },
        {
          title: "Recent topics",
          voices: [
            "Suspendisse placerat eros iaculis ex dictum efficitur.",
            "Nam consectetur tellus nec elit posuere, luctus bibendum nisl fermentum.",
            "Nullam ornare erat quis lorem fermentum, eu dapibus velit mattis.",
            "Proin quis odio vitae nulla ultrices vulputate et eu elit.",
          ],
        },
        {
          title: "Latest replies",
          voices: [
            "Suspendisse non risus ut libero bibendum posuere ut molestie metus.",
            "Nam imperdiet ex ornare erat quis nec scelerisque ultricies.",
            "Suspendisse lobortis lectus a nisl pharetra, commodo volutpat eros porttitor.",
            "Nulla suscipit odio vitae nulla velit id placerat varius.",
          ],
        },
      ],
    };
  },
  methods: {
    changeActive(index) {
      this.headerMenu.forEach((element) => {
        element.active = false;
      });
      if (this.headerMenu[index].active) {
        this.headerMenu[index].active = false;
      } else if (!this.headerMenu[index].active) {
        this.headerMenu[index].active = true;
      }
    },
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

.ms_back-to-top {
  color: white;
  background-color: rgba(0, 0, 0, 0.7);
  display: inline-block;
  padding: 0.2rem 1rem;
  border-radius: 4px 4px 0px 0px;
  position: fixed;
  bottom: 0;
  right: 75px;
}

.ms_back-to-top:hover {
  color: white;
}
</style>
