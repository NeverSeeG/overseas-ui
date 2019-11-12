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
           axios.get('/api/goods/findAll').then(function(res){
               alert(res);
               console.log(res)
           }).catch(function(res){
               alert(res);
           })
       } 
    }
  }
</script>