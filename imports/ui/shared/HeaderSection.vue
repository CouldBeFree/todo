<template>
  <section class="todoapp">
    <header class="header">
      <h1>Simple todos</h1>
      <input @keypress.enter="addNewTodo" v-model="name" class="new-todo" type="text" placeholder="Type todo">
    </header>
  </section>
</template>

<script>
  import { Todos } from '../../api/todos';
  
  export default {
    name: "HeaderSection",
    data(){
      return{
        name: ''
      }
    },
    methods: {
      async addNewTodo(){
        const newTodo = {
          name: this.name,
          date: new Date(),
          completed: false
        };
        
        await Todos.insert(newTodo);
        this.name = '';
      }
    }
  }
</script>

<style scoped>

</style>
