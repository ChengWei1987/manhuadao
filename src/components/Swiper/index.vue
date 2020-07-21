<template>
  <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">Slide 1</div>
        <div class="swiper-slide">Slide 2</div>
        <div class="swiper-slide">Slide 3</div>
      </div>
      <!-- 如果需要分页器 -->
      <div class="swiper-pagination"></div>
    </div>
</template>

<script>
import Swiper from 'swiper'
import 'swiper/swiper.scss'

export default {
  name: 'Swiper',
  mounted () {
    /* eslint-disable */
    new Swiper(".swiper-container", {
      pagination: {
        el: ".swiper-pagination",
      }
    });
    /* eslint-enable */
  }

}
</script>

<style lang="scss" >
  .swiper-container {
    width: 100%;
    height: 180px;
    .swiper-pagination-bullet {
      opacity: 1;
      vertical-align: middle;
      width: 6px;
      height: 6px;
      margin: 0 5px;
      border-radius: 50%;
      background-color: hsla(0, 0%, 100%, .7);
    }
    .swiper-pagination-bullet-active {
      width: 20px;
      height: 10px;
      background: url('../../assets/icon/dot.png') no-repeat;
      background-size: 100%;
    }
  }
</style>
