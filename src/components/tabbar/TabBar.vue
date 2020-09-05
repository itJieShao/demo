<template>
  <ul class="tabbar">
      <li v-for="item in tabBarList" @click="itemClick(item.path)">
          <img :src="item.path == $route.path ? item.activeIcon : item.icon" alt="">
          <p :style="item.path == $route.path ? 'color:red' : ''">{{item.text}}</p>
      </li>
  </ul>
</template>

<script>
export default {
    name:'tabbar',
    data(){
        return {
            tabBarList:[
                {
                    path:'/',
                    text:'首页',
                    icon:require('@/assets/images/tab-home.png'),
                    activeIcon:require('@/assets/images/tab-home-current.png'),
                },
                {
                    path:'/category',
                    text:'分类  ',
                    icon:require('@/assets/images/tab-cate.png'),
                    activeIcon:require('@/assets/images/tab-cate-current.png'),
                },
                {
                    path:'/cart',
                    text:'购物车',
                    icon:require('@/assets/images/tab-cart.png'),
                    activeIcon:require('@/assets/images/tab-cart-current.png'),
                },
                {
                    path:'/user',
                    text:'我的',
                    icon:require('@/assets/images/tab-my.png'),
                    activeIcon:require('@/assets/images/tab-my-current.png'),
                },
            ]
        }
    },
    methods:{
        itemClick(path){
            if (this.$route.path != path) this.$router.replace(path)
        }
    }
}
</script>

<style scoped>
    .tabbar{
        position: fixed;
        bottom: 0;
        display: flex;
        width: 3.75rem;
        height: .54rem;
        border-top: .01rem solid #ddd;
    }
    .tabbar li{
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: .14rem;
        color: #666;
    }
    .tabbar li img{
        width: .25rem;
        height: .25rem;
    }
</style>