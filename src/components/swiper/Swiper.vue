<template>
   <swiper :options="swiperOption">

    <swiper-slide>1</swiper-slide>

    <swiper-slide>1</swiper-slide>

    <swiper-slide>1</swiper-slide>

  </swiper>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    name:'swiper',
    components: {
      swiper,
      swiperSlide
    },
    data () {
    return {
      swiperOption:{
        slidesPerView: 'auto',
        centeredSlides:true,
        spaceBetween: 10,
        loop:true,
        speed:600, //config参数同swiper4,与官网一致
      }
    }
  },
}
</script>

<style>

</style>