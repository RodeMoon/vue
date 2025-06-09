<template>
  <div>
    <h1>MAIN</h1>
    <p>this is the new text.</p>
    <img src="../images/square.jpg" alt="Square lee" width="250px"/>
    <p>This is a square Lee.</p>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
h1 {
  color: rgb(188, 240, 158);
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  font-family: 'Courier New', Courier, monospace;
}
p {
  color: rgb(0, 0, 0);
  background-color: rgb(202, 254, 195);
  padding: 10px;
  border-radius: 5px;
  font-weight: bold;
  font-size: 24px;
  text-decoration: underline;
  text-decoration-color: rgb(0, 0, 0);
  text-decoration-thickness: 2px;
  text-decoration-style: wavy;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  font-family: 'Courier New', Courier, monospace;
  line-height: 1.5;
  letter-spacing: 1px;
  word-spacing: 2px;
}
div {
  background-color: black;
  padding: 10px;
  border-radius: 5px;
}
h1,
p {
  text-align: center;
}
img {
  display: block;
  margin: 0 auto;
  border-radius: 10px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
