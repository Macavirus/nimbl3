<template>
  <div class="nav">
    <ul class=nav>
      <li class="nav__li" v-for="item in navItems">
        <img class="nav__icon" :src="item.icon">
        <span class="nav__text">{{ item.name }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      navItems: [
        {
          name: 'Dashboard',
          icon: './static/icons/controls-white.svg'
        },
        {
          name: 'Orders',
          icon: './static/icons/shopping-cart-white.svg'
        },
        {
          name: 'Companies',
          icon: './static/icons/factory-white.svg'
        },
        {
          name: 'Products',
          icon: './static/icons/box-white.svg'
        },
        {
          name: 'Documents',
          icon: './static/icons/document-white.svg'
        },
        {
          name: 'Pricing',
          icon: './static/icons/pricing-label-white.svg'
        },
        {
          name: 'Brands',
          icon: './static/icons/shapes-white.svg'
        },
        {
          name: 'Settings',
          icon: './static/icons/gear-white.svg'
        },
        {
          name: 'Reports',
          icon: './static/icons/chart-white.svg'
        },
        {
          name: 'Account Users',
          icon: './static/icons/people-white.svg'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style style="scss" scoped>
.nav {
  background-color: #702283;
  box-shadow: 8px 0 8px 0 rgba(0, 0, 0, 0.21);
  color: #FFFFFF;
  font-family: Montserrat, sans-serif;
  font-size: 14px;
  font-weight: 600;
  line-height: 34px;
  width: 246px;
}

.nav__li {
  display: flex;
  align-items: center;
}

.nav__icon {
  margin-left: 30px;
  width: 17px;
  height: 17px;
}

.nav__text {
  margin-left: 26px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  height: 67px;
}
</style>
