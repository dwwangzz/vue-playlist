<template>
  <footer>
    <p>{{copyright}}</p>
  </footer>
</template>

<script>
  export default {
    name: 'app-footer',
    data() {
      return {
        copyright: 'Copyright 2019 Vue Demo'
      }
    }
  }
</script>

<!-- css 作用域，有scoped属性之后就只作用于当前页面 -->
<style scoped>
  footer {
    background-color: #666;
    padding: 6px;
  }
  p {
    padding: 10px;
    text-align: center;
    color: #fff;
  }
</style>
