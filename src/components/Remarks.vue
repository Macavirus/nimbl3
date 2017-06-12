<template>
  <div class="remarks">
    <div class="remarks__title">
      Remarks
    </div>
    <div class="remarks__box">
      {{ remarks }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'remarks',
  data () {
    return {
      remarks: 'When you enter into any new area of science, you almost always find yourself with a baffling new language of technical terms to learn before you can converse with the experts. This is certainly true in astronomy both in terms of terms that refer to the cosmos and terms that describe the tools of the trade, the most prevalent being the telescope. So to get us off of first base, let’s define some of the key terms that pertain to telescopes to help you be able to talk to them more intelligently.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.remarks {
  text-align: left;
}

.remarks__title {
  color: #333333;
  font-family: Montserrat;
  font-size: 12px;
  line-height: 16px;
  margin: 14px 0;
}

.remarks__box {
  border: 1px solid #D8D8D8;
  border-radius: 3px;
  background-color: #FFFFFF;
  color: #8899AA;
  font-family: Montserrat;
  font-size: 11px;
  line-height: 17px;
  padding: 15px 19px 17px;
  margin-right: 17px;
}
</style>
