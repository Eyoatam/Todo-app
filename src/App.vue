<template>
  <div id="app">
        <Header />
    <notifications group="cool" closeOnClick="true" position="top right" width="300px" speed="400" type="success"/>
    <router-view />
  </div>
</template>

<script>
import Header from "./components/layouts/Header";
export default {
  name: "app",
  components: {
    Header,
  },
};
</script>

<style>
@import url("https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css");
@import url("https://fonts.googleapis.com/css2?family=Nunito:wght@400;700&display=swap");
#app {
background-image: linear-gradient(to top, #30cfd0 0%, #330867 100%);
  font-family: "Nunito", sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #42b983;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.todo-item {
  background: #fff;
}

.isComplete {
  text-decoration: line-through;
}

.del {
  cursor: pointer;
  float: right;
}

li {
  list-style: none;
}

.holder {
  background: #fff;
}

li {
  padding: 20px;
  font-size: 1.3em;
  background-color: #e0edf4;
  border-left: 5px solid #3eb3f6;
  margin-bottom: 2px;
  color: #3e5252;
  list-style: none;
}

p {
  text-align: center;
  padding: 30px 0px;
  color: gray;
}

.container {
  box-shadow: 0px 0px 40px lightgray;
}

i {
  float: right;
  cursor: pointer;
}