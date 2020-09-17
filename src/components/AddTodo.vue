<template>
  <div>
    <form @submit.prevent="addTodo">
      <input
        type="text"
        v-model="title"
        name="title"
        class="input"
        placeholder="Add Todo..."
      />
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false,
      };
      this.$notify({
        group: "cool",
        type: "success",
        title: "Todo Successfully <b> content </b> Added",
      });
      // Send up to parent
      this.$emit("add-todo", newTodo);
      this.title = "";
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  margin-bottom: 1rem;
}
input[type="text"] {
  flex: 10;
  padding: 5px;
}
.input {
  width: calc(100% - 60px);
  min-height: 50px;
  border: 0;
  border-radius: 5px;
  padding: 15rem;
  font-size: 1.3em;
  background-color: #343a40;
  outline: none;
  transition: 300ms ease-in-out;
  /* margin-right: 1rem; */
  color: aliceblue;
}
input[type="submit"] {
  flex: 2;
}

button {
  background: transparent;
  border: 1px solid;
  border-radius: 50%;
}
</style>
