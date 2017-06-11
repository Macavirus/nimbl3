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
.orderspec {
  display: flex;
  align-items: center;
  width: 100%;
}

.orderspec__order {
  height: 80px;
  width: 822px;
  border: 1px solid rgba(173, 179, 185, 0.51);
  border-radius: 3px;
  background-color: #FFFFFF;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.orderspec__contact {
  margin-left: 15px;
  text-align: left;
}

.orderspec__contact--name {
  margin: 0;
  color: #626272;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: bold;
  line-height: 21px;
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

  &:hover {
    background: #626272;
  }
}

.orderspec__type {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  padding: 0;

  &::after {
    content: '';
    box-sizing: border-box;
    height: 34px;
    width: 2px;
    border: 1px solid #ADB3B9;
    opacity: 0.2;

    position: absolute;
    right: -28px;
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

.orderspec__label {
  height: 15px;
  width: 59.16px;
  color: #626272;
  font-family: Montserrat;
  font-size: 11px;
  font-weight: bold;
  line-height: 15px;
  text-align: center;
  margin: 0;
  margin-bottom: 3px;
}

.orderspec__selector {
  box-sizing: border-box;
  height: 33px;
  width: 111.15px;
  border: 1px solid #C9C9C9;
  border-radius: 4px;
  background-color: #FFFFFF;
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
