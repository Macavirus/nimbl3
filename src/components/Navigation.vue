<template>
  <div class="nav">
    <div class="nav__logo">
      <img class="nav__logo--image" src="static/icons/logo-white.svg">
    </div>
    <div class="nav__user">
      <p class="nav__user--greeting">
        Hello, {{ user.name }}
      </p>
      <p class="nav__user--company">
        {{ user.company }}
      </p>
    </div>
    <ul class=nav>
      <li class="nav__li" v-for="item in navItems">
        <a class="nav__link" v-bind:class="{ active: item.isActive }" href="">
          <img class="nav__icon" :src="item.icon">
          <span class="nav__text">{{ item.name }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      user: {
        name: 'Somchai',
        company: 'Twin Types Corporation'
      },
      navItems: [
        {
          name: 'Dashboard',
          icon: './static/icons/controls-white.svg',
          isActive: true
        },
        {
          name: 'Orders',
          icon: './static/icons/shopping-cart-purple.svg'
        },
        {
          name: 'Companies',
          icon: './static/icons/factory-purple.svg'
        },
        {
          name: 'Products',
          icon: './static/icons/box-purple.svg'
        },
        {
          name: 'Documents',
          icon: './static/icons/document-purple.svg'
        },
        {
          name: 'Pricing',
          icon: './static/icons/pricing-label-purple.svg'
        },
        {
          name: 'Brands',
          icon: './static/icons/shapes-purple.svg'
        },
        {
          name: 'Settings',
          icon: './static/icons/gear-purple.svg'
        },
        {
          name: 'Reports',
          icon: './static/icons/chart-purple.svg'
        },
        {
          name: 'Account Users',
          icon: './static/icons/people-purple.svg'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style style="sass" scoped>
.nav {
  background-color: #702283;
  box-shadow: 8px 0 8px 0 rgba(0, 0, 0, 0.21);
  color: #FFFFFF;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 600;
  line-height: 34px;
  width: 246px;
  margin: 0;
}

.nav__logo {
  height: 70px;
  width: 246px;
  background-color: #4C1367;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav__logo--image {
  height: 50px;
  width: 158px;
  margin: 0;
  padding: 0;
}

.nav__user {
  box-sizing: border-box;
  height: 45px;
  width: 246px;
  background-color: #FFFFFF;
  text-align: left;
  padding-left: 21px;
  position: relative;
}

.nav__user--greeting {
  color: #DF542A;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  line-height: 18px;
  margin: 0;
  padding-top: 5px;
}

.nav__user--company {
  color: #626272;
  font-family: 'Montserrat', sans-serif;
  font-size: 11px;
  font-weight: 600;
  line-height: 14px;
  margin: 0;
  padding-top: 3px;
  text-transform: uppercase;
}

.nav__link {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #D18EE2;
}

.nav__link:hover {
  background: rgba(76, 19, 103, 0.5);
}

.nav__li {}

.nav__icon {
  margin-left: 30px;
  width: 17px;
  height: 17px;
}

.nav__text {
  margin-left: 26px;
}

.active {
  background: rgba(76, 19, 103, 0.5);
  color: #FFFFFF;
  box-shadow: 0 -1px 0 0 #4C1367, 0 1px 0 0 #4C1367;
  position: relative;
}

.active::before {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  content: '';
  height: 41px;
  width: 6px;
  border-radius: 0 17px 17px 0;
  background-color: #FFCC00;
  z-index: 100;
}


ul {
  list-style-type: none;
  padding: 0;
}

li {
  height: 67px;
}
</style>
