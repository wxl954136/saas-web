<!--模板结构 -->
<template>
  <div id="app">
    <h1>hello www.youxueyou.cn ！ {{title}}</h1>
    <users-id></users-id>
  </div>
</template>

<!--处理结构  -->

<script>
import Users from './components/Users'
export default {
  name: 'App',
  data(){
    return {
      title:"this my first vue"
    }
  },
  components:{
    "users-id":Users //注意标签名:users-id
  }
}
</script>
<!--解决样式 -->
<style>
#app {

}
</style>
