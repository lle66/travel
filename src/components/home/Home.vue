<template>
  <div>
    <Header :city="city"></Header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
    <!-- <p style="font-size:6px">home</p>
    <router-link to="/list">List</router-link>-->
  </div>
</template>

<script>
import Header from "./homeComponents/Header";
import HomeSwiper from "./homeComponents/Swiper";
import HomeIcons from "./homeComponents/Icons";
import HomeRecommend from "./homeComponents/Recommend";
import HomeWeekend from "./homeComponents/Weekend";
import axios from "axios";
export default {
  name: "Home",
  data() {
    return {
      city: "ppoooooooooooo",
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    };
  },
  components: {
    Header,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
    getHomeInfo() {
      axios
        .get("/api/index.json") //请求一个url
        .then(this.getHomeInfoSucc); //axios返回结果是个promise对象
    },
    getHomeInfoSucc(res) {
      res = res.data;
      if (res.ret && res.data) {
        const data = res.data;
         this.city=data.city
         this.swiperList=data.swiperList
         this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted() {
    this.getHomeInfo();
  }
};
</script>

<style scoped>
</style>
