<template>
  <div class="App">
    <Todos v-bind:todos="todos"/>
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
import Todos from "./components/Todo/Todos";
import AddTodo from "./components/Todo/AddTodo";

export default {
 name: "App",
 components:{
   Todos,
   AddTodo
 },
 data(){
   return{
           todos: [
        {
          id: 1,
          title: 'Go workout',
          completed: false
        },
        {
          id: 2,
          title: 'Do laundry',
          completed: false
        },
        {
          id: 3,
          title: 'Cook food',
          completed: false
        },
        {
          id: 4,
          title: 'Clean up room',
          completed: false
        },
        {
          i: 5,
          title: 'Finish work',
          completed: false
        }
      ]
   }
 }
}
</script>

<style>

</style>