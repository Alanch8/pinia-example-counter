<template>
  <h2>El count es: {{ counterStore.oddOrEven }}</h2>
</template>

<script setup>
import { useCounterStore } from "../stores/counter";

const counterStore = useCounterStore();
</script>

<style></style>
