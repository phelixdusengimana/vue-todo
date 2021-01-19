<template>
  <div class="todos">
      <h1>Todos app</h1>
      <ul>
        <li v-for="todo in todos" v-bind:key="todo.id">
          <Todo v-bind:todo="todo"/>
        </li>
      </ul>
  </div>
</template>

<script>
import Todo from "./Todo";
export default {
  name: "Todos",
  components: {
    Todo
  },
  props:[
      "todos"
  ]
    
}
</script>

<style>

</style>