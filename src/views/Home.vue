<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <input class="search_btn" type="text" placeholder="请输入关键词搜索" disabled>
      <swiper ref="mySwiper" :options="swiperOptions">
        <swiper-slide v-for="item in banner">
          <img :src="item.img" alt="">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper> 
      <!-- <button ref="btn">点击</button> -->
      <ul class="cate-content">
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
        <li class="cate-item">
          <img src="@/assets/images/temp/c1.png" alt="">
          <p>环球美食</p>
        </li>
      </ul>
    </div>
  </div>
</template>


<script>
import BScroll from 'better-scroll'
export default {
  data(){
    return {
      banner:[
        {img:require('@/assets/images/temp/banner1.jpg')},
        {img:require('@/assets/images/temp/banner2.jpg')},
        {img:require('@/assets/images/temp/banner3.jpg')}
      ],
      swiperOptions: {
        pagination:'.swiper-pagination',
        loop:true
      }
    }
  },
  mounted(){
    new BScroll(this.$refs.wrapper);
    // console.log(this.$refs.btn.getBoundingClientRect().top)
  },
  created(){
    console.log(this.$route.query)
  }
}
</script>

<style scoped>
  .wrapper{
    height: calc(100vh - .54rem);
    overflow: hidden;
  }
  .content{
    position: relative;
  }
  .swiper-container,.swiper-slide img{
    width: 3.75rem;
    height: 1.875rem; 
  }
  /* button{
    width: 1rem;
    height: 0.3rem;
    background: red;
    color: #fff;
    border: none;
    border-radius: 0.15rem;
    margin: 0 auto !important;
  } */
  .search_btn{
    position: absolute;
    width: 3.2rem;
    height: 0.25rem;
    top: 0.15rem;
    left: 0.275rem;
    background-color: rgba(255,255,255,.6);
    border-radius: 0.18rem;
    border: none;
    z-index: 100;
    color: #606266;
    text-align: center;
  }
  .cate-content{
    width: 3.5rem;
    display: flex;
    flex-wrap: wrap;
    margin: 0.1rem auto;
  }
  .cate-item{
    width: 0.7rem;
    height: 0.75rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .cate-item img{
    width: 0.4rem;
    height: 0.4rem;
  }
  .cate-item p{
    font-size: 0.14rem;
    color: #666;
    margin-top: 0.05rem;
  }
</style>