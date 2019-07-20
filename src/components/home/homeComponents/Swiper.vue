<template>
<div class='wrapper'><swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class='swiper-img' :src="item.imgUrl" alt="">
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
    <!-- <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div> -->
    <!-- <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
  </swiper></div>
  
</template>

<script>
export default {
name:'HomeSwiper',
data(){
    return{
      swiperOption:{
          pagination:'.swiper-pagination',
          loop:true
      } ,
      swiperList:[
          {
              id:'0001',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/ae8987bff39ff10e82675a3643154e66.jpg_750x200_0f187b2e.jpg'
          },{
              id:'0002',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg'
          }
      ]
    }
}
}

</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
      background :#fff  
.wrapper
   overflow:hidden
   width:100%
   height:0
   padding-bottom:31.25%
   .swiper-img
      width:100%
</style>
