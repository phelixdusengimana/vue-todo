<template>
    <div class="add__todo">
       <form @submit="addTodo">
           <input type="text" name="title" v-model="title"/>
           <button type="submit">Add &#x2b;</button>
       </form>
    </div>
</template>

<script>
import uuid from "uuid";
export default {
    name: "AddTodo",
    data() {
        return{
            title: ''
        }
    },
    methods:{
        addTodo(e){
            e.preventDefault();
            const newTodo = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
        }
    }
}
</script>
<style scoped>

</style>