<template>
  <div id="app">
    <navigation></navigation>
    <div class="main">
      <orderspec></orderspec>
      <addproduct></addproduct>
    </div>
  </div>
</template>

<script>
import Navigation from './components/Navigation'
import Orderspec from './components/Orderspec'
import Addproduct from './components/Addproduct'

export default {
  name: 'app',
  components: {
    Navigation,
    Orderspec,
    Addproduct
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
  background: #F4F7F8;
}
* {
  box-sizing: border-box;
}
a {
  text-decoration: none;
  color: inherit;
}
button {
  border: 0;
  margin: 0;
  padding: 0;
  text-align: inherit;
  text-transform: inherit;
  font: inherit;
  -webkit-font-smoothing: inherit;
  letter-spacing: inherit;
  background: none;
  cursor: pointer;
  overflow: visible;
}
::-moz-focus-inner {
  border: 0;
  padding: 0;
}
#app {
  text-align: center;
  color: #2c3e50;
  display: flex;
}
.main {
  margin-left: 34px;
  margin-top: 50px;
}
</style>
