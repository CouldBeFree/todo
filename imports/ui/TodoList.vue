<template>
  <ul class="todo-list">
    <todo
      v-for="todo in todos"
      :key="todo._id"
      :todo="todo"
      @toggleCheck="handleToggleCheck"
      @removeTodo="deleteTodo"
    ></todo>
  </ul>
</template>

<script>
  import Todo from './Todo'
  import { Todos } from '../api/todos';

  export default {
    props: ['todos'],
    name: "TodoList",
    components: {
      Todo
    },
    methods: {
      async handleToggleCheck(todo){
        await Todos.update(todo.id, { $set: { completed:
          todo.completed }})
      },
      async deleteTodo(id){
        await Todos.remove(id);
      }
    }
  }
</script>

<style scoped>

</style>
