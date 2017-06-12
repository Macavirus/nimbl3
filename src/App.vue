<template>
  <div id="app">
    <navigation></navigation>
    <div class="main">
      <orderspec></orderspec>
      <addproduct></addproduct>
      <orderlisting></orderlisting>
    </div>
  </div>
</template>

<script>
import Navigation from './components/Navigation'
import Orderspec from './components/Orderspec'
import Addproduct from './components/Addproduct'
import Orderlisting from './components/Orderlisting'

export default {
  name: 'app',
  components: {
    Navigation,
    Orderspec,
    Addproduct,
    Orderlisting
  }
}
</script>

<style lang="scss">
@import 'assets/base';
@import 'assets/fonts';
</style>
