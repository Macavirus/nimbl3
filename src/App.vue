<template>
  <div id="app">
    <div class="nav__wrap">
      <navigation></navigation>
    </div>
    <div class="main">
      <orderspec></orderspec>
      <addproduct></addproduct>
      <orderlisting></orderlisting>
      <remarks></remarks>
    </div>
  </div>
</template>

<script>
import Navigation from './components/Navigation'
import Orderspec from './components/Orderspec'
import Addproduct from './components/Addproduct'
import Orderlisting from './components/Orderlisting'
import Remarks from './components/Remarks'

export default {
  name: 'app',
  components: {
    Navigation,
    Orderspec,
    Addproduct,
    Orderlisting,
    Remarks
  }
}
</script>

<style lang="scss">
@import 'assets/breakpoints';
@import 'assets/base';
@import 'assets/fonts';
</style>
