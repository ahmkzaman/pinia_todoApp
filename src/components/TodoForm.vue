<script setup>
import { ref } from "vue"
import { todoStore } from '../store/todoStore'

const todo = ref("")
const store = todoStore()

function addItemAndClear(item) {
    if (item.length === 0) {
        return
    }
    store.addTodo(item)
    todo.value = ''
}
</script>

<template>
    <form @submit.prevent="addItemAndClear(todo)">
        <input v-model="todo" type="text" /><button class="button">Add</button>
    </form>
</template>

<style scoped>

input {
  border: 1px solid #ccc; 
  padding: 8px 12px; 
  font-size: 16px; 
  border-radius: 4px; 
}
input:focus {
  outline: none; 
  border-color: #e72cc1; 
  box-shadow: 0 0 5px rgba(232, 75, 217, 0.5); 
}
.button {
  display: inline-block;
  padding: 10px 20px;
  margin-left: 5px;
  font-size: 14px;
  text-align: center;
  text-decoration: none;
  border-radius: 6px;
  background-color: #3498db; 
  color: #ffffff;
  border: 2px solid #3498db; 
  transition: background-color 0.3s, color 0.3s, border-color 0.3s;
  cursor: pointer;
}

.button:hover {
  background-color: #2980b9; 
  color: #ffffff; 
  border-color: #2980b9;
}


</style>