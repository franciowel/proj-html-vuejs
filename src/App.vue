<template>
  <div id="app">
    <HeaderComponents :headerLinks="headerLinks"/>
    <JumbotronComponent/>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue'
import JumbotronComponent from './components/JumboTronComponent.vue'

export default {
  data () {
    return {
      headerLinks: [
        {
          text: 'Home',
          link: '#'
        },
        {
          text: 'About',
          link: '#'
        },
        {
          text: 'Services',
          link: '#'
        },
        {
          text: 'Blog',
          link: '#'
        },
        {
          text: 'Contact',
          link: '#'
        },
        {
          text: 'Portfolio',
          link: '#'
        },
      ],
    }
  },
  name: 'App',
  components: {
    HeaderComponents,
    JumbotronComponent,
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
