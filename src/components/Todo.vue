<template>
  <div class="hello">
    <h1>Todo App</h1>
    <input
      @keyup.enter="addTodo"
      v-model="title"
      type="text"
      placeholder="What do you want to do?"
    />
    <button @click="addTodo">Send</button>
    <ul>
      <li :key="index" v-for="(todo, index) in todos">
        {{ todo }} <span class="remove" @click="removeTodo">&times;</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Todo",
  data() {
    return {
      title: "",
      todos: ["Go to the market"],
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.title);
      this.title = "";
    },
    removeTodo(id) {
      this.todos.splice(id, 1)
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 5px;
}
a {
  color: #42b983;
}
.remove{
  border-radius: 100%;
  padding: 5px;
  margin-left: 10px;
  background-color: rgb(255,0, 0);
  cursor: pointer;
  margin-bottom: 5px;
}

</style>
