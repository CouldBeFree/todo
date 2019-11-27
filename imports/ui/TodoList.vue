<template>
  <ul>
    <todo
      v-for="todo in todos"
      :key="todo._id"
      :todo="todo"
    ></todo>
  </ul>
</template>

<script>
  import Todo from './Todo'

  export default {
    props: ['todos'],
    name: "TodoList",
    components: {
      Todo
    }
  }
</script>

<style scoped>

</style>
