<!-- ColorChangerComponent.vue -->
<template>
    <div :style="{ backgroundColor: bgColor }" class="color-changer">
      <button @click="changeColor">Cambiar Color de Fondo</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        bgColor: 'white'
      };
    },
    methods: {
      changeColor() {
        const colors = ['red', 'blue', 'green', 'yellow', 'pink', 'purple'];
        this.bgColor = colors[Math.floor(Math.random() * colors.length)];
      }
    }
  };
  </script>
  
  <style scoped>
  .color-changer {
    padding: 20px;
    text-align: center;
  }
  </style>
  