<!-- App.vue -->
<template>
  <div id="app">
    <h1>Proyecto Vue</h1>
    <h2>Integrantes del equipo</h2>
    <ul>
      <li>Darlin Mariela Ramos Gutierrez SMSS172422</li>
      <li>Anderson Jose Berrios Diaz SMSS100222</li>
    </ul>

    <h2>Componentes</h2>
    <div class="component-section">
      <h3>Contador</h3>
      <CounterComponent />

      <TodoListComponent />

      <h3>Cambiador de Color</h3>
      <ColorChangerComponent />
    </div>
  </div>
</template>

<script>
import CounterComponent from './components/CounterComponent.vue';
import TodoListComponent from './components/TodoListComponent.vue';
import ColorChangerComponent from './components/ColorChangerComponent.vue';

export default {
  name: 'App',
  components: {
    CounterComponent,
    TodoListComponent,
    ColorChangerComponent
  }
};
</script>

<style>
body {
  background-color: #f0f8ff; 
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  list-style-type: none;
  padding: 0;
}

.component-section {
  margin-top: 20px;
}

.component-section > div {
  margin-bottom: 20px;
}

.component-section h3 {
  margin-bottom: 10px;
}
</style>
