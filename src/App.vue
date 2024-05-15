<script setup>
  var task = {
    name: '',
    date: '',
  }
  var tasks = [];

  function addTask(){
    tasks.push(task)
    console.log(tasks[0].name + tasks[0].date)
  }
</script>

<template>
 <div class="container">
  <div class="form-container">
    <label for="name">Tarefa</label>
    <input name="name" type="text" v-model="task.name">
    <label for="date">Data</label>
    <input name="date" type="date" v-model="task.date">
    <button v-on:click="addTask">Cadastrar</button>
  </div>
</div>

</template>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: lightgreen;
}

.form-container {
  width: 400px;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="date"],
button {
  width: 100%;
  margin-bottom: 10px;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

body {
  margin: 0;
  padding: 0;
}
</style>