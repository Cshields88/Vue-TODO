<template>
<div>
  <todo-list :todos="todos"></todo-list>
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
    TodoList
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

/* li {
  display: inline-block;
  margin: 0 10px;
} */

a {
  color: #42b983;
}
</style>
