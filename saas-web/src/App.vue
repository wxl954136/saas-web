<!--模板结构 -->
<template>
  <div id="app">
    <app-header></app-header>
    <h1>hello www.youxueyou.cn ！ {{title}}</h1>
    <users-id></users-id>
  </div>
</template>

<!--处理结构  -->

<script>
import Users from './components/Users'
import Header from  './components/Header'
export default {
  name: 'App',
  data(){
    return {
      title:"this my first vue"
    }
  },
  components:{
    "users-id":Users, //注意标签名:users-id
    "app-header":Header
  }
}
</script>
<!--解决样式 -->
<style scoped>
  h1{
    color:red;
  }
</style>
