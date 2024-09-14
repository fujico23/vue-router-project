<script setup>
import { ref } from 'vue'
const count = ref(0)
function countUp(event, times) {
  count.value = event.clientX * times
}
</script>

<template>
  <div id="app">
    <button @click="topPage">トップページ!!</button>
    <button @click="sabPage">サブページ</button>
    <button @click="userListPage">ユーザー一覧ページ</button>
    <button @click="userListPage">ユーザー一覧ページ!</button>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  methods: {
    topPage() {
      this.$router.push({ name: 'home' });
    },
    SubPage() {
      this.$router.push({ name: 'SubPage' });
    },
    userListPage() {
      this.$router.push({ name: 'UserList', query: { redirect: true } });
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
