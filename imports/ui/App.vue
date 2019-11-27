<template>
  <section class="todoapp">
    <header-section></header-section>
    <main-section :todos="todos"></main-section>
    <footer-section :todos="todos"></footer-section>
  </section>
</template>

<script>
  import Header from './shared/HeaderSection'
  import Footer from './shared/FooterSection'
  import Main from './shared/MainSection'

  import { Todos } from '../api/todos'

  export default{
    data(){
      return{

      }
    },
    components: {
      "header-section": Header,
      "footer-section": Footer,
      "main-section": Main
    },
    meteor: {
      $subscribe: {
        ['todos']: [],
      },
      todos(){
        return Todos.find({});
      }
    }
  }
</script>

<style>

</style>
