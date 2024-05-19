<!-- CounterComponent.vue -->
<template>
  <div>
    <h2>Contador: {{ count }}</h2>
    <button @click="increment">Incrementar</button>
    <button @click="decrement">Decrementar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    }
  }
};
</script>
