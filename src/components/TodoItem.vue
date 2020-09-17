<template>
  <div class="holder" :class="{ isComplete: todo.completed }">
    <li>
      <input type="checkbox" @change="markComplete" class="input" />
      {{ todo.title }}
      <i class="fa fa-trash del" @click="$emit('del-todo', todo.id)"></i>
    </li>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>

<style scoped>
@import url("https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css");
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
  background-image: linear-gradient(to top, #30cfd0 0%, #330867 100%);
}

input {
  transition: 300ms ease-in-out;
}

li {
  padding: 20px;
  font-size: 1.3em;
  background-color: #e0edf4;
  border-left: 5px solid #466980;
  margin-bottom: 2px;
  color: #425858;
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
</style>
