<template>
  <div class="container">
    <h1>About page</h1>
    <button @click="counterStore.increment">{{ counterStore.counter }}</button>
    <OddOrEven />
  </div>
</template>

<script setup>
import { useCounterStore } from "../stores/counter";
import OddOrEven from "../components/OddOrEven.vue";

const counterStore = useCounterStore();
</script>

<style scoped>
.container {
  text-align: center;
}

h1 {
  font-weight: bold;
}

h2 {
  font-size: 80px;
}

button {
  margin: 20px;
  font-size: 50px;
}

input {
  width: 50px;
  text-align: center;
  font-size: 50px;
  margin: 20px;
}
</style>
