<template>
  <div id="app">
    <div class="leftbox">
      <!-- 3.使用组件 -->
      <Leftbox msg="Welcome to Your Vue.js App"/>
    </div>
    <!-- <div class="rightContent">
        <router-view></router-view>
    </div> -->
  </div>
</template>

<script>
// 1.引入组件
import Leftbox from './components/index.vue'

export default {
  name: 'App',
  // 2.挂载组件实例
  components: {
    Leftbox
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
}
#app .leftBar{
  width:20vw;
  border-right:5px solid red;
  margin-right:10px;
}
#app .rightContent{
    /* width:80vw; */
    flex: 1;
    height:90vh;
    /* background: #fdffcb; */
    /* font-size:40px; */
}
/* 屏幕宽度小于992px，则执行如下样式，样式权重要高于其他的样式*/
@media screen and (max-width:992px){
  #app .leftBar{
   display: none;
  }
}
</style>
