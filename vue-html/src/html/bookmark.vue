<template>
  <div>
    <h1 id="titulo_principal">Lenguajes de Programación</h1>
    <a href="#Java">Java</a> | <a href="#Python">Python</a> |
    <a href="#JavaScript">JavaScript</a>
    <div id="Java" class="tarjeta">
      <h2>Java</h2>
      <p><span class="titulo">Creador:</span> James Gosling</p>
    </div>
    <div id="Python" class="tarjeta">
      <h2>Python</h2>
      <p><span class="titulo">Creador:</span> Guido van Rossum</p>
    </div>
    <div id="JavaScript" class="tarjeta">
      <h2>JavaScript</h2>
      <p><span class="titulo">Creador:</span> Brendan Eich</p>
    </div>
    <div>
      <h2>Resumen Lenguajes de Programación</h2>
      <p>www.globalmentoring.com.mx</p>
    </div>
    <a href="#Java">Java</a> | <a href="#Python">Python</a> |
    <a href="#JavaScript">JavaScript</a>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
/*identificador css*/
#titulo_principal {
  color: #f72585;
  text-align: center;
  margin: 15px;
}
h2 {
  color: #3f37c9;
}
p {
  color: #457b9d;
}
/*Clase de CSS*/
.tarjeta {
  border: 10px solid #560bad;
  background-color: #f1faee;
  text-align: center;
  margin: 10px 115px;
  padding: 15px;
}
.titulo {
  color: #f72585;
}
</style>
