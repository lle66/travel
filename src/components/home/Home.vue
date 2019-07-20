<template>
  <div>
    <Header></Header>
    <div><span>111</span><a href="">2222</a></div>
    <!-- <p style="font-size:6px">home</p>
    <router-link to="/list">List</router-link> -->
  </div>
</template>

<script>
import Header from './homeComponents/Header'
export default {
  name: 'Home',
  components:{Header},
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
