<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add todo</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{todo.value}}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>

<script>
 let id = 0
 export default {
   data(){
     return {
       newTodo: '',
       todos: [
         {id: id++, value: "Hippos"},
         {id: id++, value: "Potamuses"},
         {id: id++, value: "Elephants"}
       ]
     }
   },
   methods: {
     addTodo(){
       this.todos.push({id: id++, value: this.newTodo})
     },
     removeTodo(todo){
       this.todos = this.todos.filter(o => o !== todo)
     }
   }
 }
</script>
