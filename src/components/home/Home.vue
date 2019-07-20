<template>
  <div>
    <Header></Header>
    <HomeSwiper></HomeSwiper>
    <!-- <p style="font-size:6px">home</p>
    <router-link to="/list">List</router-link> -->
  </div>
</template>

<script>
import Header from './homeComponents/Header'
import HomeSwiper from './homeComponents/Swiper'
export default {
  name: 'Home',
  components:{Header, HomeSwiper},
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
