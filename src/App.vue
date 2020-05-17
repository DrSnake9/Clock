<template>
  <div id="app">

<Clock></Clock>
  </div>
</template>

<script>
import Clock from './components/Clock.vue'

export default {
  name: 'App',
  components: {
    Clock
  },
  methods: {
    getLocale () {
      if (navigator.languages && navigator.languages.length) {
        return navigator.languages[0]
      } else {
        return navigator.language
      }
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
