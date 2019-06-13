<template>
  <div class="users">
    <ul>
      <li v-for="(user,index) in users">
        {{user}} | {{index}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'users',
    data() {
      return {
        users: ['全局组件', '张三', '李四', '王五']
      }
    }
  }
</script>

<style scoped>

</style>
