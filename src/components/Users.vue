<template>
  <div class="users">
    <h1 v-on:click="title='title已经改变'">用户列表 | {{title}}</h1>
    <ul>
      <li v-for="(user,index) in users"
          v-on:click="user.show = !user.show">
        <h2>{{user.name}}</h2>
        <h3 v-show="user.show">{{user.job}}</h3>
      </li>
    </ul>
    <button @click="users.pop()">删除一个</button>
  </div>
</template>

<!--
  传值：string、number、boolean ，改变一个，其他的不会跟随改变
  引用：array、object ，改变一个，所有的都会跟着改变
-->
<script>
  export default {
    name: 'users',
    // props: ["users"],
    props: {
      users: {
        type: Array,
        required: true
      },
      title: {
        type: String
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
