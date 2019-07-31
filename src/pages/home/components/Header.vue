<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe892;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe611;</span>
      输入城市名查询
    </div>
    <div class="header-right">
      <span class="iconfont arrow-icon">&#xe6aa;</span>
      修改
    </div>
  </div>
</template>
<script>
export default {
  name: "HomeHeader"
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    height: 0.64rem;
    line-height: 0.64rem;
    margin-top: 0.12rem;
    margin-left: 0.2rem;
    padding-left: 0.15rem;
    background-color: #fff;
    border-radius: 0.1rem;
    color: #ccc;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;

    .arrow-icon {
      margin-left: -0.04rem;
      font-size: 0.24rem;
    }
  }
}
</style>
