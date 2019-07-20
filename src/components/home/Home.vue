<template>
  <div>
    <Header></Header>
    <home-swiper></home-swiper>
<home-icons></home-icons>
    <!-- <p style="font-size:6px">home</p>
    <router-link to="/list">List</router-link> -->
  </div>
</template>

<script>
import Header from './homeComponents/Header'
import HomeSwiper from './homeComponents/Swiper'
import HomeIcons from './homeComponents/Icons'
export default {
  name: 'Home',
  components:{
    Header, 
    HomeSwiper,
    HomeIcons},
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
