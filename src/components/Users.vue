<template>
  <div class="users">
    <h1>用户列表</h1>
    <ul>
      <li v-for="(user,index) in users"
          v-on:click="user.show = !user.show">
        <h2>{{user.name}}</h2>
        <h3 v-show="user.show">{{user.job}}</h3>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'users',
    data() {
      return {
        users: [
          {name: "张三", job: "收垃圾的", show: false},
          {name: "李四", job: "开奔驰的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false},
          {name: "王五", job: "开公司的", show: false}
        ]
      }
    }
  }
</script>

<style scoped>
  .users {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
  }

  li {
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
    cursor: pointer;
  }

  li:active {
    cursor: default;
  }
</style>
