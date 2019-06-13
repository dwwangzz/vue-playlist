<!-- 1. 模板：html结构 -->
<template>
  <div id="app">
    <app-header></app-header>
    <users></users>
    <app-footer></app-footer>
    <!-- 局部组件 -->
    <!-- <HelloWorld /> -->
    <!-- 全局组件 -->
    <!-- <users /> -->
  </div>
</template>

<!-- 2. 行为：处理逻辑 -->
<script>
  // 局部注册组件
  import HelloWorld from './components/HelloWorld'
  import Header from './components/Header'
  import Footer from './components/Footer'

  export default {
    name: 'App',
    // 局部注册组件
    components: {
      HelloWorld,
      // 自定义组件名称
      "app-header": Header,
      "app-footer": Footer
    }
  }
</script>

<!-- 3. 样式：解决样式 -->
<style>
  * {
    padding: 0;
    margin: 0;
  }
</style>
<style scoped>
  h1 {
    color: #f40;
  }
</style>
