<template>
  <div class="orderspec">
    <div class="orderspec__order">
      <div class="orderspec__contact">
        <h3 class="orderspec__contact--name">
          {{ contact.name }}
        </h3>
        <div class="orderspec__contact--address">
          {{ contact.address }}
        </div>
        <div class="orderspec__contact--tel">
          {{ contact.tel }}
        </div>
      </div>
      <div class="orderspec__type">
        <h4 class="orderspec__label">
          Type
        </h4>
        <select class="orderspec__selector">
          <option v-for="option in type">
            {{ option.text }}
          </option>
        </select>
      </div>
      <div class="orderspec__type">
        <h4 class="orderspec__label">
          Owned By
        </h4>
        <select class="orderspec__selector">
          <option v-for="option in owner">
            {{ option.name }}
          </option>
        </select>
      </div>
      <div class="orderspec__type">
        <h4 class="orderspec__label">
          Status
        </h4>
        <select class="orderspec__selector">
          <option v-for="option in status">
            {{ option.text }}
          </option>
        </select>
      </div>
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
      contact: {
        name: 'CPF Saraburi',
        address: 'Highway 2, Kaeng Khoi Saraburi Thailand',
        tel: '+66 087 348 79 34'
      },
      type: [
        { text: 'Retailers' },
        { text: 'Consumers' }
      ],
      owner: [
        { name: 'Tom Hanks' },
        { name: 'Tom Cruise' },
        { name: 'Tom Selleck' }
      ],
      status: [
        { text: 'Pending' },
        { text: 'Started' },
        { text: 'Finished' }
      ]
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../assets/breakpoints';
.orderspec {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  flex-direction: column;
  width: 100%;
  @include mq(tab) {
    flex-direction: row;
    justify-content: space-between;
  }
}

.orderspec__order {
  min-height: 80px;
  height: 100%;
  padding-bottom: 10px;
  border: 1px solid rgba(173, 179, 185, 0.51);
  border-radius: 3px;
  background-color: #F4F7F8;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;

  @include mq(tab) {
    padding-top: 10px;
    background-color: #FFFFFF;
  }
  @include mq(desk) {
    margin-right: 17px;
  }
}

.orderspec__contact {
  text-align: center;
  width: 100%;
  padding: 16px 0 13px;
  box-shadow: 0 -1px 3px 0 rgba(0, 0, 0, 0.11), 0 2px 3px 0 rgba(98, 98, 114, 0.21);
  background-color: #FFFFFF;

  @include mq(tab) {
    margin-left: 15px;
    text-align: left;
    width: auto;
    box-shadow: none;
  }
}

.orderspec__contact--name {
  margin: 0;
  color: #626272;
  font-family: Montserrat;
  font-weight: bold;

  font-size: 24px;
  line-height: 29px;
  @include mq(tab) {
    font-size: 16px;
    line-height: 21px;
  }
}

.orderspec__contact--address {
  color: #8899AA;
  font-family: Montserrat;
  font-size: 12px;
  line-height: 16px;
}

.orderspec__contact--tel {
  color: #8899AA;
  font-family: Montserrat;
  font-size: 12px;
  font-weight: 600;
  line-height: 15px;
  padding-top: 5px;
  display: none;

  @include mq(tab) {
    display: inherit;
  }
}

.orderspec__back {
  height: 18px;
  width: 36px;
  color: #626272;
  font-family: Montserrat;
  font-size: 14px;
  line-height: 19px;
  margin-left: 25px;
  margin-right: 25px;
  display: none;

  @include mq(tab) {
    display: inherit;
  }
}

.orderspec__update {
  height: 44px;
  width: 140px;
  border-radius: 5px;
  background-color: #8899AA;
  color: #FBFBFB;
  font-family: Montserrat;
  font-size: 14px;
  line-height: 19px;
  margin: 10px 0;

  &:hover {
    background: #626272;
  }
}

.orderspec__type {
  display: flex;
  flex-direction: column;
  align-items: left;
  position: relative;
  padding: 0;
  width: 100%;
  margin: 0 15px;

  @include mq(tab) {
    width: 100%;
    align-items: center;
  }


  @include mq(desk) {

    width: auto;
    min-width: 111px;

    &::after {
      content: '';
      box-sizing: border-box;
      height: 34px;
      width: 2px;
      border: 1px solid #ADB3B9;
      opacity: 0.2;

      position: absolute;
      right: -18px;
      top: 50%;
      transform: translateY(-50%);
    }

    &:last-of-type {
      margin-right: 19.5px;
    }

    &:last-of-type::after {
      height: 0;
      width: 0;
      border: 0;
    }
  }
}

.orderspec__label {
  height: 15px;
  color: #626272;
  font-family: Montserrat;
  margin: 15px 0 9px;
  font-size: 13px;
  line-height: 16px;
  text-align: left;
  font-weight: initial;

  @include mq(tab) {
    font-size: 11px;
    line-height: 15px;
    text-align: center;

    font-weight: bold;
    margin-bottom: 3px;
  }
}

.orderspec__selector {
  box-sizing: border-box;
  height: 33px;
  border: 1px solid #C9C9C9;
  border-radius: 4px;
  background-color: #FFFFFF;
  width: 100%;
}

select {
  height: 15px;
  width: 64.26px;
  color: #8899AA;
  font-family: Montserrat;
  font-size: 11px;
  line-height: 15px;
}

.orderspec__selector option {
  height: 15px;
  width: 64.26px;
  color: #8899AA;
  font-family: Montserrat;
  font-size: 11px;
  line-height: 15px;
}
</style>
