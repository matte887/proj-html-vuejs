<template>
  <div id="app">
    
    <!-- header + jumbotron -->
    <AppHeader :navItems = 'headerMenu' />
    <!-- /header + jumbotron -->

    <!-- Main -->
    <AppMain />
    <!-- /Main -->

    <!-- Footer -->
    <AppFooter :footerItems = 'footerMenu' />
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
      headerMenu: ['Home', 'Apple', 'Microsoft', 'Android', 'Forums', 'Contact us'],
      footerMenu: [
        {
          title: 'Popular topics',
          voices: [
            'Morbi id velit fermentum, faucibus mauris ac, condimentum magna.', 
            'Ut nec ante quis ex fermentum iaculis vel id orci.',
            'Nullam in mi eu augue egestas congue ut ac sem.',
            'Donec mollis nisi ac aliquet finibus.'
          ]
        },
        {
          title: 'Recent topics',
          voices: [
            'Suspendisse placerat eros iaculis ex dictum efficitur.', 
            'Nam consectetur tellus nec elit posuere, luctus bibendum nisl fermentum.',
            'Nullam ornare erat quis lorem fermentum, eu dapibus velit mattis.',
            'Proin quis odio vitae nulla ultrices vulputate et eu elit.'
          ]
        },
        {
          title: 'Latest replies',
          voices: [
            'Suspendisse non risus ut libero bibendum posuere ut molestie metus.', 
            'Nam imperdiet ex ornare erat quis nec scelerisque ultricies.',
            'Suspendisse lobortis lectus a nisl pharetra, commodo volutpat eros porttitor.',
            'Nulla suscipit odio vitae nulla velit id placerat varius.'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
@import './style/variables.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';
</style>
