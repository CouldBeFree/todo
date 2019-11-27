<template>
  <section class="main">
    <input class="toggle-all" type="checkbox">
    <todo-list :todos="todos"></todo-list>
  </section>
</template>

<script>
  import TodoList from "../TodoList";

  export default {
    props: ['todos'],
    name: "MainSection",
    components: {
      TodoList
    }
  }
</script>

<style scoped>

</style>
