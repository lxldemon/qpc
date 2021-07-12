<template>
  <div id="app">
      <el-container>
          <el-header>
              <Header></Header>
          </el-header>
          <el-main>
              <router-view></router-view>
          </el-main>
          <el-footer style="height: 50px">
              <Footer></Footer>
          </el-footer>
      </el-container>
  </div>
</template>
<script>
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'
  export default {
    components:{
      Header,Footer
    }
  }
</script>
<style lang="scss">
body {
    margin: 0;
    padding: 0;
    background: #f4f6f8;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
.el-header, {
    background-color:#222;
    color: #333;
    text-align: center;
    line-height: 60px;
    padding: 0px;

}
.el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
}
.el-footer {
    background-color: #555;
    color: #333;
    height: 50px;
    text-align: center;
    line-height: 50px;
}
::-webkit-scrollbar
{
    width: 5px;
}

/*定义滚动条轨道 内阴影+圆角*/
::-webkit-scrollbar-track
{
    border-radius: 10px;
    background-color: rgba(0,0,0,0.1);
}

/*定义滑块 内阴影+圆角*/
::-webkit-scrollbar-thumb
{
    border-radius: 10px;
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
    background-color: rgba(0,0,0,0.1);
}
</style>
