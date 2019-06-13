<template>
  <header>
    <h1>{{title}}</h1>
  </header>
</template>

<script>
  export default {
    name: 'app-header',
    data() {
      return {
        title: 'Vue.js Demo'
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
