<script setup>

import TodoForm from './components/TodoForm.vue'
import TodoList from './components/TodoList.vue'


</script>

<template>

  <div class="box">
    <h1>Todo List</h1>
  <div class="todo-app">
    
    <TodoForm />
    <TodoList />
  </div>
  </div>
  
</template>


<style scoped>

.box {
  width: 500px;
  height: 600px;
  border: 2px solid #333; 
  border-radius: 10px;
  background-color: #f0f0f0; 
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2); 
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: column;
  
  align-items: center;
}

h1 {
  font-size: 36px; 
  color: #eb2724; 
  text-align: center; 
  text-transform: uppercase; 
  font-family: 'Arial', sans-serif; 
  letter-spacing: 2px; 
  margin-bottom: 20px; 
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.todo-app {
  border-radius: 10px;
  padding: 5vh;
  width: 25vw;
  background-color: #e4d3e8;
}
</style>
