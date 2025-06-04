<template>
  <div>
    <h1>Welcome to Vue Coffee</h1>
    <section>
      <h3>Count: {{ count }}</h3>
      <h3>Square: {{ square }}</h3>
      <button @click="count++">+ 1</button>
      <button @click="count--">- 1</button>
    </section>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';
const count = ref(0);
const square = computed(() => count.value * count.value);
</script>

<style scoped></style>