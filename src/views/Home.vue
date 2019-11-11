<template>
  <div >
    <h2>Home Page</h2>
    <el-button type="primary" @click="testAxios()">测试axios调用</el-button>
  </div>
</template>
<script>
  import axios from 'axios'
  export default {
    name: 'Home',
    methods: {
       testAxios() {
           axios.get('http://localhost:8686/goods/findAll').then(function(res){
               alert(res)
           }).catch(function(res){
               alert(res);
           })
       } 
    }
  }
</script>