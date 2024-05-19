<!-- TodoListComponent.vue -->
<template>
  <div>
    <h3>Lista de Tareas</h3>
    <input v-model="newTodo" @keyup.enter="addTodo" placeholder="Agregar nueva tarea">
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        {{ todo }}
        <button @click="deleteTodo(index)">Eliminar</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: '',
      todos: []
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim() !== '') {
        this.todos.push(this.newTodo);
        this.newTodo = '';
      }
    },
    deleteTodo(index) {
      this.todos.splice(index, 1);
    }
  }
};
</script>
