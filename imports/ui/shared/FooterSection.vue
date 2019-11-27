<template>
  <footer class="footer">
    <span class="todo-count">
      <strong>23424 elements</strong>
    </span>
    <ul class="filters">
      <li><a href="/">All</a></li>
      <li><a href="/">Active</a></li>
      <li><a href="/">Completed</a></li>
    </ul>
    <button class="clear-completed"></button>
  </footer>
</template>

<script>
  export default {
    name: "FooterSection"
  }
</script>

<style scoped>
  button{
    display: none;
  }
</style>
