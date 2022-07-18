<template>
  <div id="app">
    <HeaderComponents :headerLinks="headerLinks"/>
    <JumbotronComponent/>
    <whatWeDo/>
    <SecondJumbo/>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue'
import JumbotronComponent from './components/JumboTronComponent.vue'
import SecondJumbo from './components/SecondJumbotron.vue'
import whatWeDo from './components/WhatWeDo.vue'

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
    whatWeDo,
    SecondJumbo,
    
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
