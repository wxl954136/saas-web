<template>
    <heade v-on:click="changeTitle">
        <h1>{{titleX}}</h1>
    </heade>

</template>

<script>
    export default {
        name: "app-Header",
        props:{
          titleX:{
            type:String
          }
        },
        data(){
            return {
                title1:"Vue.js ---- >  Header Demo"
            }
        },
        methods:{
            changeTitle:function () {
              // this.titleX = "我想喝水"
                this.$emit("titleChangedX","son to parent !!!!")
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
