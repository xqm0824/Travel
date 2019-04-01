<template>
  <div>
    <div class="banner" @click="hanleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1412/77/cb5a5c0c47e96f6b42ce646cddf4af0d.water.jpg_600x330_17d4b9aa.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          鸟巢(AAAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          6
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-if="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['//img1.qunarzz.com/sight/p0/1412/77/cb5a5c0c47e96f6b42ce646cddf4af0d.water.jpg_600x330_17d4b9aa.jpg', 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_r_800x800_6edd8174.jpg']
    }
  },
  methods: {
    hanleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom 0
    line-height: .6rem
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    color: #fff
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      height: .32rem
      line-height: .32rem
      margin-top: .14rem
      padding: 0 .4rem
      border-radius: .2rem
      background: rgba(0, 0, 0, .8)
      font-size: .24rem
      .banner-icon
        font-size: .24rem
</style>
