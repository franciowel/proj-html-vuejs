<template>
  <div id="app">
    <HeaderComponents :headerLinks="headerLinks"/>
    <JumbotronComponent/>
    <whatDo/>
    <SecondJumbo/>
    <sliderCarousel/>
    <SponsorComponent/>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue'
import JumbotronComponent from './components/JumboTronComponent.vue'
import SecondJumbo from './components/SecondJumbotron.vue'
import whatDo from './components/WhatDo.vue'
import sliderCarousel from './components/Carousel.vue'
import SponsorComponent from './components/SponsorComponent.vue'


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
    whatDo,
    SecondJumbo,
    sliderCarousel,
    SponsorComponent,
    
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
