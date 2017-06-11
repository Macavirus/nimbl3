<template>
  <div class="orderspec">
    <div class="orderspec__order"> test
    </div>
      <button class="orderspec__back">
        Back
      </button>
      <button class="orderspec__update">
        Update Order
      </button>
    </div>
</template>

<script>
export default {
  name: 'orderspec',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.orderspec {
  display: flex;
  align-items: center;
  padding-left: 34px;
}

.orderspec__order {
	height: 80px;
	width: 822px;
	border: 1px solid rgba(173,179,185,0.51);
	border-radius: 3px;
	background-color: #FFFFFF;
}

.orderspec__update {
  	height: 44px;	width: 140px;	border-radius: 5px;	background-color: #8899AA;
    	color: #FBFBFB;	font-family: Montserrat;	font-size: 14px;	line-height: 19px;
}
</style>
