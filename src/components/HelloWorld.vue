<template>
  <el-container>
    <el-header class="header">
      <div></div>
    </el-header>  
    <el-main>
      <div class="title">详细信息</div>
      <el-tabs v-model="activeName">
          <el-tab-pane label="药品" name="first">药品</el-tab-pane>
          <el-tab-pane label="化妆品" name="second">化妆品</el-tab-pane>
          <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
      </el-tabs>
      <el-card class="box-card">
        <div slot="header"  class="clearfix">
          <span class="word">111</span>
         
        </div>
        <div v-for="index in 4" :key='index' class="text">
          {{index}}
        </div>
        
      </el-card>
      <el-card class="box-card">
          <div slot="header"  class="clearfix">
            <span class="word">111</span>
           
          </div>
          <div v-for="index in 4" :key='index' class="text">
            {{index}}
          </div>
          
        </el-card>
    </el-main>
   
  </el-container>
  <!-- <el-input-number v-model="num1" @change="handleChange" :min="1" :max="10" label="描述文字"></el-input-number> -->
</template>

<script>

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      num1: 1,
      activeName: 'first'
    }
  },
  methods: {
    handleChange (value) {
      console.log(value)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
  background: url('../assets/header.png') no-repeat 100% 100%;
  width:100%;
  height:100px!important;
  background-size: 100%;
}
.title{
  width: 100%;
  height:30px;
  line-height: 30px;
  background: #eee;
  text-align: left;
}
.clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }
.box-card {
    width: 100%;
  }
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
