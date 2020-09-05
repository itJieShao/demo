<template>
  <div>
    <h1>我的</h1>
    <button @click="go">关于我们</button>
  </div>
</template>
<script>
    export default {
        name:'user',
        methods:{
            go(){
              this.$router.push('/?id=1')
            }
        }
    }
</script>
