<template>
  <li class="todo" :class="{ completed: todo.completed }">
    <div class="view">
      <input @click="toggleCheck" v-if="todo.completed" class="toggle" type="checkbox" checked>
      <input @click="toggleCheck" v-else class="toggle" type="checkbox">
      <label>{{todo.name}}</label>
      <button class="destroy" @click="$emit('removeTodo', todo._id)"></button>
    </div>
  </li>
</template>

<script>
  export default {
    props: ['todo'],
    name: "Todo",
    methods: {
      toggleCheck(){
        this.$emit('toggleCheck', {
          id: this.todo._id,
          completed: !this.todo.completed
        })
      }
    }
  }
</script>

<style scoped>

</style>
