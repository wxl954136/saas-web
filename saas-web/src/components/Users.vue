<template>
   <div id = "Users">
      <h1>用户列表</h1>
      <ul>
          <li v-for="user in UsersX" v-on:click="user.show = !user.show">
            <h2>{{user.name}}</h2>
            <h3 v-show="user.show">{{user.age}}</h3>
          </li>
      </ul>
     <button v-on:click="deleteUser">删除</button>
   </div>
</template>

<script>
    export default {
        name: "Users",
       // props:["UsersX"],
        props:{
          UsersX:{
            type:Array,
            required:true
          }
        },
        data(){
          return {

          }
        },
        methods:{
          deleteUser:function () {
              this.UsersX.pop();
          }
        }
    }
</script>

<style scoped>
  h1{
    color:blue;
  }
</style>
