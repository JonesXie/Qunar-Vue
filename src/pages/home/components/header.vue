<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.currentCity}}
        <span class="iconfont arrow-icon">&#xe61e;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState({
      currentCity: 'city'
    })
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    line-height: $headerHigh
    background-color: $bgColor
    color:#fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align : center
        font-size : .4rem
    .header-input
      flex:1
      height: .64rem
      line-height: .64rem
      margin-top: 0.12rem
      margin-left : .2rem
      padding-left : 0.2rem
      background: #ffffff
      border-radius: 0.1rem
      color : #ccc
    .header-right
      min-width: 1.04rem
      padding 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left : -0.04rem
        font-size : 0.24rem
</style>
