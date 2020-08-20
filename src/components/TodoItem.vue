<template>
  <div class="todo-item" :class="{ isComplete: todo.completed }">
    <p>
      <b-container>
        <input type="checkbox" @change="markComplete" />
        {{ todo.title }}
        <button @click="$emit('del-todo', todo.id)" class="del">x</button>
      </b-container>
    </p>
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
.todo-item {
  background: #e9ecef;
  padding: 20px;
  border-bottom: 1px dotted #ccc;
}

.isComplete {
  text-decoration: line-through;
}

.del {
  background: #dc3545;
  color: #fff;
  border: none;
  padding: 0px 8px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}
</style>
