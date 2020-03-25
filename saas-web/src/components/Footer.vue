<template>
  <header>
    <h1>{{titleX}}</h1>
  </header>

</template>

<script>
  export default {
    name: "app-Footer",
    props:{
      titleX:{
        type:String
      }
    },
    data(){
      return {
        title1:"company copyright 2020-03-29"
      }
    }
  }
</script>

<style scoped>
  header{
    background:gray;
    padding: 10px;
  }
</style>
