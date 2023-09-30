<script setup>
import { todoStore } from "../store/todoStore";
import { storeToRefs } from "pinia";

const store = todoStore()
const { todoList } = storeToRefs(store)
const { toggleCompleted, deleteTodo } = store

</script>

<template>
    <div v-for="todo in todoList" :key="todo.id">
        <div>
            
            <input type="checkbox" v-model="todo.completed">
            <label :class="{ completed: todo.completed }" id="listTodo">{{ todo.item }}</label>
            <button @click="deleteTodo(todo.id)">Delete</button>

        </div>
    </div>
</template>

<style scoped>
#listTodo {
  font-size: 20px;
  margin-bottom: 30px; 
  border-radius: 4px;
  padding: 5px;
  border-bottom: 1px solid #ddd;
  font-weight: bold;
  color: rgb(18, 4, 62);
  
 }
button{
    cursor: pointer;
    margin-left: 10px;
    color: red;
    font-weight: bold;
    background-color: rgb(235, 210, 201);
    border-radius: 4px;
}

input {
  cursor: pointer;
  
}
.completed {
    text-decoration: line-through;
}
</style>