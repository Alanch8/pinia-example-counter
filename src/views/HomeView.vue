<template>
  <main>
    <div class="container">
      <h1>Counter</h1>
      <h2>{{ count }}</h2>
      <button @click="decreaseCount">--</button>
      <button @click="increaseCount">++</button>
      <h2>El count es: {{ oddOrEven }}</h2>
    </div>
  </main>
</template>

<script setup>
import { ref, computed } from "vue";

const count = ref(100);

const increaseCount = () => {
  count.value++;
};

const decreaseCount = () => {
  count.value--;
};

const oddOrEven = computed(() => {
  if (count.value % 2 === 0) return "Even";
  else return "Odd";
});
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
  margin: 5px;
  font-size: 70px;
}
</style>
