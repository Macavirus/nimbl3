<template>
  <div class="addproduct">
    <img class="addproduct__icon" v-bind:class="{ rotate: isRotated }" src="static/icons/icon_plus.svg">
    <form class="addproduct__form" @focusin="isRotated = !isRotated" @focusout="isRotated = !isRotated">
      <input class="addproduct__input" v-model="message" placeholder="Add Products">
    </form>
  
  </div>
</template>

<script>
export default {
  name: 'addproduct',
  data () {
    return {
      message: '',
      isRotated: false
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.addproduct {
  height: 50px;
  width: 100%;
  border: 1px solid #C3C8CD;
  border-radius: 3px;
  background-color: #FFFFFF;
  margin-top: 17px;
  display: flex;
  align-items: center;
}

.addproduct__icon {
  height: 20px;
  width: 20px;
  margin-left: 14px;
  margin-right: 14px;
  transition: all 0.2s ease-out;
}

.rotate {
  transform: rotate(-45deg);
}

.addproduct__form {
  border: 0;
  width: 100%;
  height: 100%;
  margin-right: 14px;
  display: flex;
  align-items: center;
}

.addproduct__input {
  border: 0;
  color: #8899AA;
  font-family: Montserrat;
  font-size: 12px;
  line-height: 16px;
  width: 100%;
  height: 100%;
  padding: 15px;

  &:focus {
    outline: 0;
  }
}

.slide-fade-enter-active {
  transition: all .3s ease;
}

.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}

.slide-fade-enter,
.slide-fade-leave-to
/* .slide-fade-leave-active for <2.1.8 */

{
  transform: translateX(10px);
  opacity: 0;
}
</style>
