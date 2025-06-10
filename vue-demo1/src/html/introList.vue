<template>
  <div>
    <h1>Listas No Ordenadas</h1>
    <ul style="list-style-type: square">
      <li>
        Juan
        <ul>
          <li>Tel. 44330011</li>
          <li>Cel. 99881122</li>
        </ul>
      </li>
      <li>Karla</li>
      <li>María</li>
      <li>
        Carlos
        <ul>
          <li>Tel. 55443399</li>
          <li>Cel. 55668811</li>
        </ul>
      </li>
    </ul>
    <h1>Listas Ordenadas</h1>
    <ol>
      <li>Juan</li>
      <li>Karla</li>
      <li>María</li>
      <li>Carlos</li>
    </ol>
    <h1>Listas de Definición</h1>
    <dl>
      <dt>Juan</dt>
      <dd>Tel. 44330011</dd>
      <dd>Cel. 99881122</dd>
      <dt>Karla</dt>
      <dd>Tel. 55443399</dd>
      <dd>Cel. 55668811</dd>
      <dt>María</dt>
      <dd>Tel. 44332211</dd>
    </dl>
    <h1>Lista de Navegación</h1>
    <ul>
      <li><a href="index.html">Inicio</a></li>
      <li><a href="contacto.html">Contacto</a></li>
      <li><a href="acerca.html">Acerca De</a></li>
    </ul>
    <h1>Lista de Navegación con Submenús</h1>
    <ul>
      <li><a href="index.html">Inicio</a></li>
      <li>
        <a href="contacto.html">Contacto</a>
        <ul>
          <li><a href="telefono.html">Teléfono</a></li>
          <li><a href="email.html">Email</a></li>
        </ul>
      </li>
      <li><a href="acerca.html">Acerca De</a></li>
      <li>
        <a href="ayuda.html">Ayuda</a>
        <ul>
          <li><a href="faq.html">Preguntas Frecuentes</a></li>
          <li><a href="soporte.html">Soporte Técnico</a></li>
        </ul>
      </li>
      <li><a href="terminos.html">Términos y Condiciones</a></li>
      <li><a href="privacidad.html">Política de Privacidad</a></li>
    </ul>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
h1 {
  color: #1d3557;
}
ul {
  list-style-type: none;
  background-color: #457b9d;
  overflow: hidden;
  margin: 0;
  padding: 0;
}
li {
  float: left;
}
li a {
  display: block;
  color: white;
  text-align: center;
  padding: 15px;
  text-decoration: none;
}
li a:hover {
  background-color: #1d3557;
}
ol {
  list-style: none;
  counter-reset: contador;
}
ol li {
  counter-increment: contador;
}

ol li::before {
  content: 'Curso ' counter(contador) ') ';
  color: #ff6f00;
}
ol li::after {
  content: '.';
}
</style>
