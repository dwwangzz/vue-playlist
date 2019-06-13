<!-- 1. 模板：html结构 -->
<template>
  <div id="app">
    <!-- 局部组件 -->
    <HelloWorld />
    <!-- 全局组件 -->
    <users />
  </div>
</template>

<!-- 2. 行为：处理逻辑 -->
<script>
  // 局部注册组件
  import HelloWorld from './components/HelloWorld'

  export default {
    name: 'App',
    // 局部注册组件
    components: {
      // 自定义组件名称
      // "hello-world": HelloWorld,
      HelloWorld
    }
  }
</script>

<!-- 3. 样式：解决样式 -->
<style>

</style>
