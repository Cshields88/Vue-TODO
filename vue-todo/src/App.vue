<template>
<div>
  <todo-list :todos="todos"></todo-list>
  <create-todo v-on:add-todo="addTodo">

</div>
  
</template>

<script>
import TodoList from "./components/TodoList.vue";
export default {
  data() {
    return {
      todos: [
        {
          title: "Todo A",
          project: "Project A",
          done: false
        },
        {
          title: "Todo B",
          project: "Project B",
          done: true
        },
        {
          title: "Todo C",
          project: "Project C",
          done: false
        },
        {
          title: "Todo D",
          project: "Project D",
          done: false
        }
      ]
    };
  },
  components: {
    TodoList,
    CreateTodo
  },
  methods: {
    addTodo(title) {
      this.todos.push({
        title,
        done: false
      });
    }
  }
};
</script>

<style>
</style>
