<template>
  <div>
    <div class="title border-bottom">热销推荐</div>
    <ul>
      <li class="item" v-for='item of recommendList' :key='item.id'>
        <img class="item-img" :src="item.imgUrl" >
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/97/974063def69779ab.img.jpg_200x200_3095b686.jpg',
        title: '宝宇伊春西岭温泉度假山庄',
        desc: '冰雪之冠，富有异国情调的美丽都市,冰雪之冠，富有异国情调的美丽都市'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/97/974063def69779ab.img.jpg_200x200_3095b686.jpg',
        title: '宝宇伊春西岭温泉度假山庄',
        desc: '冰雪之冠，富有异国情调的美丽都市,冰雪之冠，富有异国情调的美丽都市'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/97/974063def69779ab.img.jpg_200x200_3095b686.jpg',
        title: '宝宇伊春西岭温泉度假山庄',
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
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex:1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
