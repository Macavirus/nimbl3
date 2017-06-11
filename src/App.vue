<template>
  <div id="app">
    <navigation></navigation>
  </div>
</template>

<script>
import Navigation from './components/Navigation'

export default {
  name: 'app',
  components: {
    Navigation
  }
}
</script>

<style lang="scss">
@import 'assets/fonts';
// Basic normalize styles
html {
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  -webkit-tap-highlight-color: transparent;
}
body {
  margin: 0;
  line-height: 1;
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
}
* {
  box-sizing: border-box;
}
a {
  text-decoration: none;
  color: inherit;
}
#app {
  text-align: center;
  color: #2c3e50;
}
</style>
