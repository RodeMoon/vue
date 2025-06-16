<template>
  <MyHeader />

  <main class="container-xl mt-5">
    <h2 class="text-center">Our collection</h2>
    <div class="row mt-5">
      <blockGuitar v-for="guitar in guitars" :key="guitar.id" v-bind:guitar="guitar" />
    </div>
  </main>

  <MyFooter />
</template>

<script setup lang="ts">
import blockGuitar from './blockGuitar.vue';
import MyHeader from './myHeader.vue';
import MyFooter from './myFooter.vue';

// Importing the guitar data from a mock database
import { db } from '../data/guitars.ts';
import { ref } from 'vue';
const guitars = ref(db);
</script>

<style scoped></style>
