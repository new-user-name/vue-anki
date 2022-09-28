<!--8, computed properties-->
<template>
  <form @submit.prevent="addTodo">
    <input v-model="textTodo">
    <button>Add todo</button>
  </form>
  <ul>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done">
      <span :class="{done : todo.done}">{{todo.text}}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <button @click="hideTodos = !hideTodos">{{hideTodos ? 'Hide completed' : 'Show all'}}</button>
</template>

<script>

let id = 0

export default {
  data() {
    return {
      textTodo: '',
      hideTodos: false,
      todos: [
        {id: id++, text: "Hippo", done: false},
        {id: id++, text: "Potamus", done: true},
        {id: id++, text: "Elephant", done: false}
      ]
    }
  },
  methods: {
    addTodo() {
      this.todos.push({id: id++, text: this.textTodo, done: false})
    },
    removeTodo(todo) {
      this.todos = this.todos.filter(o => o !== todo)
    }
  },

  computed: {
    filteredTodos() {
      return this.hideTodos ? this.todos : this.todos.filter (o => !o.done)
    }
  }

}
</script>

<style>
  .done {
    text-decoration: line-through;
  }
</style>
