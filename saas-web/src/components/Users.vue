<template>
   <div id = "Users">
      <h1>用户列表</h1>
      <ul>
          <li v-for="user in Users">
                {{user}}
          </li>
      </ul>
   </div>
</template>

<script>
    export default {
        name: "Users",
        data(){
          return {
             Users:["王晓陆","姚静","王怿恒"]
          }
        }
    }
</script>

<style scoped>
  h1{
    color:blue;
  }
</style>
