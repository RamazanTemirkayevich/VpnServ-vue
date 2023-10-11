<template>
  <div class="app">
    <Header/>
    <Hero/>
    <About/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    About
  }
}
</script>