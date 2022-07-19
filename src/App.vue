<template>
  <div id="app">
    <HeaderComponents :headerLinks="headerLinks"/>
    <JumbotronComponent/>
    <whatDo/>
    <SecondJumbo/>
    <sliderCarousel/>
    <SponsorComponent/>
    <FooterComponent :quickLinks="quickLinks" :resourcesLinks="resourcesLinks"/>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue'
import JumbotronComponent from './components/JumboTronComponent.vue'
import SecondJumbo from './components/SecondJumbotron.vue'
import whatDo from './components/WhatDo.vue'
import sliderCarousel from './components/Carousel.vue'
import SponsorComponent from './components/SponsorComponent.vue'
import FooterComponent from './components/FooterComponents.vue'


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
      quickLinks: [
        {
          text: 'Services',
          link: '#'
        },
        {
          text: 'Contact',
          link: '#'
        },
        {
          text: 'Blog',
          link: '#'
        },
      ],
      resourcesLinks: [
        {
          text: 'Art Design',
          link: '#'
        },
        {
          text: 'Computer',
          link: '#'
        },
        {
          text: 'IT News',
          link: '#'
        },
        {
          text: 'Networking',
          link: '#'
        },
        {
          text: 'Web Security',
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
    FooterComponent,
    
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
