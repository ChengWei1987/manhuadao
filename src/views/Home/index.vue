<template>
  <div class="page-home">
    <!-- 首页的头部  开始 -->
    <header class="index-header">
      <a href="mine.html?cpid=0">
        <div class="header-user">
          <div class="user-btn"></div>
        </div>
      </a>
      <div class="header-logo"></div>
      <a href="search.html?cpid=0">
        <div class="header-search"></div>
      </a>
    </header>
    <!-- 首页的头部 结束 -->

    <!-- 轮播图的 开始 -->
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">Slide 1</div>
        <div class="swiper-slide">Slide 2</div>
        <div class="swiper-slide">Slide 3</div>
      </div>
      <!-- 如果需要分页器 -->
      <div class="swiper-pagination"></div>
    </div>
    <!-- 轮播图的 结束 -->
  </div>
</template>

<script>
// 引入swiper的核心和样式
import Swiper from 'swiper'
import 'swiper/swiper.scss'

export default {
  name: 'Home',
  mounted () {
    // 此时不允许出现new关键字但是不得不用,就需要eslint的注释方法来解决
    /* eslint-disable */
    new Swiper(".swiper-container", {
      pagination: {
        el: ".swiper-pagination"
      }
    });
    /* eslint-enable */
  }
}
</script>
<style lang="scss" scoped>
.page-home {
  display: flex;
  flex-direction: column;
  height: 100%;

  .index-header {
    display: flex;
    height: 44px;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
    box-sizing: border-box;
    .user-btn {
      width: 25px;
      height: 25px;
      background: url("../../assets/images/person.png") no-repeat;
      background-size: 100%;
    }
    .header-logo {
      width: 92px;
      height: 28px;
      background: url(../../assets/logo.png) no-repeat;
      background-size: 100%;
    }
    .header-search {
      width: 25px;
      height: 25px;
      background: url(../../assets/images/search.png) no-repeat;
      background-size: 100%;
    }
  }
  .swiper-container {
    width: 100%;
    height: 180px;
  }
}
</style>
