<!--模板结构 -->
<template>
  <div id="app">
    <!--子向父传值的方法 -->
    <app-header v-on:titleChangedX = "updatedTitle($event)"   v-bind:titleX="title"></app-header>
    <h1>hello www.youxueyou.cn ！ {{title}}</h1>
    <users-id v-bind:UsersX="Users"></users-id>
    <!--父向子传值的方法 -->
    <app-footer v-bind:titleX="title"></app-footer>
  </div>
</template>

<!--处理结构  -->

<script>
import Users from './components/Users'
import Header from  './components/Header'
import Footer from './components/Footer'
export default {
  name: 'App',
  data(){
    return {
      title:"值传递",
      Users:[
        {name:"王晓陆",age:42,show:true},
        {name:"姚静",age:40,show:true},
        {name:"王怿恒",age:15,show:true},
      ],
    }
  },
  methods:{
    updatedTitle:function (t_title) {
        this.title = t_title;
    }
  },
  components:{
    "users-id":Users, //注意标签名:users-id
    "app-header":Header,
    "app-footer":Footer,
  }
}
</script>
<!--解决样式 -->
<style scoped>
  h1{
    color:red;
  }
</style>
