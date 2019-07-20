<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt />
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
  name: "HomeWeekend",
  data() {
    return {
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "北京欢乐谷",
          desc: "近期小伙伴们收藏最！多！的景点"
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "北京欢乐谷",
          desc: "近期小伙伴们收藏最！多！的景点"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "北京欢乐谷",
          desc: "近期小伙伴们收藏最！多！的景点"
        }
      ]
    };
  }
};
</script>
<style lang='stylus' scoped>
@import '~styles/mixins.styl'
.title
  margin-top 0.2rem
  line-height 0.8rem
  background #eee
  tet-indent 0.2rem
.item-img-wrapper
  height 0
  overflow hidden
  padding-bottom 33.9%
  .item-img
    width 100%
.item-title
  line-height 0.54rem
  font-size 0.32rem
  ellipsis()
.item-desc
  line-height 0.4rem
  color #ccc
  ellipsis()
</style>
