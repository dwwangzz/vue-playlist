<!-- 1. 模板：html结构 -->
<template>
  <div id="app">
    <app-header v-on:titleChanged="updateTitle($event)"></app-header>
    <!-- 属性传值：父组件传到子组件 -->
    <users v-bind:users="users2" v-bind:title="title"></users>
    <users v-bind:users="users2" v-bind:title="title"></users>
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
    },
    data() {
      return {
        users2: [
          {name: "张三", job: "收垃圾的", show: false},
          {name: "李四", job: "开奔驰的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false}
        ],
        title: "父组件传值给子组件，请点击查看效果"
      }
    },
    methods: {
      updateTitle: function (title) {
        this.title = title;
      }
    },
    beforeCreate: function () {
      console.log('beforeCreate');
    },
    created: function () {
      console.log('created');
    },
    beforeMount: function () {
      console.log('beforeMount');
    },
    mounted: function () {
      console.log('mounted');
    },
    beforeUpdate: function () {
      console.log('beforeUpdate');
    },
    updated: function () {
      console.log('updated');
    },
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
