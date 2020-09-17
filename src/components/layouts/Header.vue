<template>
  <header class="header">
    <h1>Vue.js TodoList</h1>
    <div id="nav">
      <router-link class="router" to="/">Home</router-link> |
      <router-link class="router" to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header {
  /* background: #343a40; */
  color: #fff;
  text-align: left;
  margin-bottom: 5rem;
}

h1 {
  padding-bottom: 1rem;
}

.router {
  color: #fff;
  padding: 0.5rem;
}
</style>
