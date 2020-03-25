<template>
    <header>
        <h1>{{title}}</h1>
    </header>

</template>

<script>
    export default {
        name: "app-Header",
        data(){
            return {
                title:"Vue.js ---- >  Header Demo"
            }
        }
    }
</script>

<style scoped>
  header{
    background:red;
    padding: 10px;
  }
</style>
