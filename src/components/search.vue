<template>
  <!-- 搜索框 -->
  <div class="search">
    <!-- 输入框 -->
    <div class="input-box">
      <input type="text" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less">
// 搜索框
.search {
  padding: 20rpx 30rpx;
  background-color: #ea4451;
  .input-box {
    position: relative;
    &::after {
      content: "搜索";
      position: absolute;
      top: 50%;
      left: 50%;
      padding-left: 50rpx;
      transform: translate(-50%, -50%);
      color: #bbb;
      font-size: 24rpx;
      background-image: url(https://ugo2.oss-cn-hangzhou.aliyuncs.com/images/icon_search%402x.png);
      background-size: auto 32rpx;
      background-repeat: no-repeat;
    }
  }
  input {
    background-color: #fff;
    height: 60rpx;
    border-radius: 10rpx;
    padding: 5rpx 20rpx;
  }
}
</style>