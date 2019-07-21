<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for='(page,index) of pages' :key='index'>
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="iconImg">
            <img :src="item.imgUrl" alt class="iconContent" />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Vue.components
export default {
  name: "HomeIcons",
props:{
    list:Array
},
  computed: {
    pages() {
      const pages = [];
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icon>>>.swiper-container
  height 0
  padding 50%
.icons
  overflow hidden
  height 0
  padding-bottom 50%
  .icon
    float left
    width 25%
    height 0
    padding-bottom 25%
    position relative
  .iconImg
    position absolute
    top 0
    right 0
    left 0
    bottom 0.44rem
    padding 0.1rem
    box-sizing border-box
    .iconContent
      display block
      height 100%
      margin 0 auto
  .icon-desc
    position absolute
    left 0
    right 0
    bottom 0
    height 0.44rem
    line-height 0.44rem
    text-align center
    color $darkTextColor
    ellipsis()
</style>