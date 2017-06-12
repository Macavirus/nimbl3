<template>
  <div class="addproduct">
    <div class="overlay" v-show="isRotated"></div>
    <div class="addproduct__wrapper">
      <img class="addproduct__icon" v-bind:class="{ rotate: isRotated }" src="static/icons/icon_plus.svg">
      <form class="addproduct__form" @focusin="addProduct" @focusout="releaseProduct">
        <input class="addproduct__input" v-model="message" placeholder="Add Products">
      </form>
    </div>
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
  },
  methods: {
    addProduct: function () {
      this.isRotated = !this.isRotated
    },
    releaseProduct: function () {
      this.isRotated = !this.isRotated
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.addproduct {
  margin-top: 17px;
  margin-right: 17px;
}

.addproduct__wrapper {
  height: 50px;
  background-color: #FFFFFF;
  width: 100%;
  border: 1px solid #C3C8CD;
  border-radius: 3px; //
  display: flex;
  align-items: center;
  position: relative;
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

.overlay {
  position: fixed;
  top: 0;
  left: 0; // background: rgba(0, 0, 0, 0.5);
  background: rgba(0, 0, 0, 0.4);
  height: 100vh;
  width: 100vw;
}
</style>
