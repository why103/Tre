<template>
  <div>
    <div class="title border-bottom">周末去哪</div>
    <ul>
      <li class="item" v-for='item of recommendList' :key='item.id'>
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" >
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/e3/e9761259adfc1d.jpg_r_640x214_21b96532.jpg',
        title: '大连海洋世界',
        desc: '冰雪之冠，富有异国情调的美丽都市,冰雪之冠，富有异国情调的美丽都市'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/e3/e9761259adfc1d.jpg_r_640x214_21b96532.jpg',
        title: '大连海洋世界',
        desc: '冰雪之冠，富有异国情调的美丽都市,冰雪之冠，富有异国情调的美丽都市'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/e3/e9761259adfc1d.jpg_r_640x214_21b96532.jpg',
        title: '大连海洋世界',
        desc: '冰雪之冠，富有异国情调的美丽都市,冰雪之冠，富有异国情调的美丽都市'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped="">
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    margin-top: .2rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
  .item-img
    width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
