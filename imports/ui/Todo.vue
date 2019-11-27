<template>
  <li class="todo">
    <div class="view">
      <input class="toggle" type="checkbox">
      <!--<input type="checkbox">-->
      <label>{{todo.name}}</label>
      <button class="destroy"></button>
    </div>
  </li>
</template>

<script>
  export default {
    props: ['todo'],
    name: "Todo"
  }
</script>

<style scoped>

</style>
