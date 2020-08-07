<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题</div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/style.scss';
.header{
  background: $bgColor;
  color: #fff;
  line-height: .86rem;
  display: flex;
  .header-left{
    float: left;
    width: .84rem;
    text-align: center;
  }
  .header-right{
    float: right;
    width: 1.24rem;
    text-align: center;
  }
  .header-input{
    flex: 1;
    height: .64rem;
    margin-top: .12rem;
    color: #ccc;
    line-height: .64rem;
    background: #fff;
    border-radius: .1rem;
    padding-left: .2rem;
  }
}
</style>
