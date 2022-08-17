<template>
  <main>
    <div class="container">
      <h1>Counter</h1>
      <h2>{{ counterStore.counter }}</h2>
      <button @click="counterStore.decrement">--</button>
      <button @click="counterStore.increment">++</button>
      <OddOrEven />
      <!-- <h2>El count es: {{ counterStore.oddOrEven }}</h2> -->
    </div>
  </main>
</template>

<script setup>
//UTILIZANDO Stores con PINIA
import { useCounterStore } from "../stores/counter";
import OddOrEven from "../components/OddOrEven.vue";

const counterStore = useCounterStore();

/*
UTILIZANDO Composition API
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

UTILIZANDO Option API (No funciona aqui):
export default {
  name: "HomeView",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increaseCount() {
      this.count++;
    },
    decreaseCount() {
      this.count--;
    },
  },
  computed() {
    oddOrEven() {
      if (this.count % 2 === 0) return "Even";
      else return "Odd"
    }
  },
};*/
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
</style>
