<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.img"/>
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
        img: 'http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '西山温泉',
        desc: '浪漫的西山温泉'
      }, {
        id: '0001',
        img: 'http://img1.qunarzz.com/sight/source/1602/9c/39c5ce9ff58609.jpg_r_640x214_efb90102.jpg',
        title: '西山温泉',
        desc: '浪漫的西山温泉'
      }, {
        id: '0001',
        img: 'http://img1.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
        title: '西山温泉',
        desc: '浪漫的西山温泉'
      }, {
        id: '0001',
        img: 'http://img1.qunarzz.com/sight/p0/1611/96/96c7b547622c8334a3.img.jpg_200x200_cd0b30b0.jpg',
        title: '西山温泉',
        desc: '浪漫的西山温泉'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins'
  .recommend-title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top: .2rem
  .item-img-wrapper
    overflow hidden
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
