<template>
  <div class="header">
    <div class="header-left">
        <div class="iconfont back-icon" ><span>&#xe77f;</span></div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe7e2;</span>
        输入城市景点游玩主题</div>
    <div class="header-right">
      {{this.city}}
        <span class="iconfont">&#xe7eb;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props:["city"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header {
    display: flex;
  line-height: 0.86rem;
  background:$bgcolor;
  color:#fff;
}

.header-left {
  width: 0.64rem;
  float:left;

   .back-icon{
       font-size:20px;
      text-align:center;
   }
}

.header-input{
    flex:1;
    line-height :.64rem;
    height :0.64rem;
  background :#fff;
  color:#ccc;
  margin-top :.12rem;
  margin-left :.2rem;
  border-radius:0.1rem;
}
.header-right {
   width: 1.24rem;
  float:right;
  text-align :center;
  padding-left 0.2rem}

</style>
