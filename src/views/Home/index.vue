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
    <!-- 轮播图 开始 -->
    <Swiper></Swiper>
    <!-- 轮播图 结束 -->
  </div>
</template>

<script>
// 引入swiper的核心和样式
// 如果使用../相对路径,如果当前组件位置发生改变
// 那么相对路径也就需要去修改,如果使用@符号别名的方式,后期就不需要修改这个提示
import Swiper from '@/components/Swiper/index'

export default {
  name: 'Home',
  components: {
    Swiper: Swiper
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
}
</style>
