<template>
  <div id="app">
    
    <!-- header + jumbotron -->
    <AppHeader :navItems = 'headerMenu' />
    <!-- /header + jumbotron -->

    <!-- Main -->
    <AppMain />
    <!-- /Main -->

    <!-- Footer -->
    <AppFooter />
    <!-- /Footer -->

  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      headerMenu: ['Home', 'Apple', 'Microsoft', 'Android', 'Forums', 'Contact us']
    }
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
@import './style/variables.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';
</style>
