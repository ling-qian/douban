<template>
  <div class="swiper-container" :class="swipeid">
    <div class="swiper-wrapper">
      <slot name="swiper-con"></slot>
    </div>
    <div :class="{'swiper-pagination':pagination}" :style="{'text-align':paginationDirection}"></div>
  </div>
</template>
<script>
  import '../assets/lib/swiper/js/swiper.js'
  export default {
    props: {
      swipeid: {
        type: String,
        default: ''
      }
      ,
      effect: {
        type: String,
        default: 'slide'
      },
      loop: {
        type: Boolean,
        default: true
      },
      direction: {
        type: String,
        default: 'horizontal'
      },
      pagination: {
        type: Boolean,
        default: true
      },
      autoplay: {
        type: Number,
        default: '5000'
      },
      paginationType: {
        type: String,
        default: 'bullets'
      },
      paginationDirection:{
        type:String,
        default:'center'
      }
    },
    mounted() {
      var That = this;
      new Swiper ('.'+That.swipeid,{
        loop: That.loop,
        pagination: '.swiper-pagination',
        paginationType: That.paginationType,
        autoplay: That.autoplay,
        direction: That.direction,
        effect: That.effect,
        autoplayDisableOnInteraction : false,
      })
    }
  }
</script>
<style>
  @import '../assets/lib/swiper/css/swiper.css';
  .swiper-container img{
    width: 100%
  }
  .swiper-pagination-bullet-active {
    background: #fff;
  }
</style>
