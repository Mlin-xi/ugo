<template>
  <div>
    <!-- 自定义组件 -->
    <search />
    <!-- 焦点图 -->
    <swiper
      class="banner"
      indicator-dots
      indicator-color="rgba(255,255,255,.3)"
      autoplay
      interval="2000"
      circular
      indicator-active-color="#ffffff"
    >
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner1.png" alt />
        </a>
      </swiper-item>
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner2.png" alt />
        </a>
      </swiper-item>
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner3.png" alt />
        </a>
      </swiper-item>
    </swiper>
    <!-- 主导航 -->
    <div class="navs">
      <a href>
        <img src="/static/uploads/icon_index_nav_1@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_2@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_3@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_4@2x.png" alt />
      </a>
    </div>
    <!-- 楼层 -->
    <div class="floors">
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor01_title.png" alt />
        </div>
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor01_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_5@2x.png" alt />
          </a>
        </div>
      </div>
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor02_title.png" alt />
        </div>
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor02_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_5@2x.png" alt />
          </a>
        </div>
      </div>
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor03_title.png" alt />
        </div>
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor03_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_5@2x.png" alt />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import search from "@/components/search";
export default {
  components: {
    search
  },
  methods: {}
};
</script>

<style scoped lang="less">
// 焦点图
.banner {
  height: 340rpx;
  a {
    height: 340rpx;
  }
}
// 导航
.navs {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20rpx 30rpx;
  background-color: #fff;
  a {
    width: 128rpx;
    height: 140rpx;
  }
}

// 楼层
.floor {
  .title {
    height: 60rpx;
    width: 750rpx;
    padding: 30rpx 0 0 15rpx;
    background-color: #f4f4f4;
  }
  .items {
    padding: 20rpx 16rpx;
    overflow: hidden;
    a {
      float: left;
      margin-left: 10rpx;

      // 前两个
      // 0 --> 2  1 --> 1  2 --> 0
      // &:nth-child(-n+2) {}
      &:nth-last-child(-n + 2) {
        margin-top: 10rpx;
      }
      &:first-child {
        width: 232rpx;
        height: 386rpx;
        margin-left: 0;
      }
      &:nth-child(2),
      &:nth-child(5) {
        width: 273rpx;
        height: 188rpx;
      }
      &:nth-child(3),
      &:nth-child(4) {
        width: 193rpx;
        height: 188rpx;
      }
    }
  }
  &:first-child {
    a {
      width: 233rpx !important;
      height: 188rpx;
    }
  }
}
</style>
