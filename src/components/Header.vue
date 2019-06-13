<template>
  <header>
    <h1 v-on:click="changeTitle">{{title}}</h1>
  </header>
</template>

<script>
  export default {
    name: 'app-header',
    data() {
      return {
        title: 'Vue.js Demo, 点击这里子组件向父组件传值'
      }
    },
    methods: {
      changeTitle: function () {
        // 在父组件中注册事件、titleChanged，参数是 '子向父组件传值'
        this.$emit("titleChanged", "子向父组件传值");
      }
    }
  }
</script>

<!-- css 作用域，有scoped属性之后就只作用于当前页面 -->
<style scoped>
  header {
    background-color: #00ff55;

  }

  h1 {
    text-align: center;
    padding: 10px;
  }

</style>
