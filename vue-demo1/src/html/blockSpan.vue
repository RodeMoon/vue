<template>
  <div>
    <h1>Elemento span (inline)</h1>
    <p>
      Texto donde vamos a
      <span style="color: #e63946; border: 1px solid black">enfatizar</span>
      y cambiar el
      <span style="color: #457b9d; font-weight: bold"> color de algunos elementos </span>
    </p>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
h1 {
  color: #f72585;
  text-align: center;
}
h2 {
  color: #3f37c9;
}
p {
  color: #457b9d;
}
div {
  border: 10px solid #560bad;
  background-color: #f1faee;
  text-align: center;
}
</style>
