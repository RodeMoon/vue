<template>
  <header>
    <h1>Etiquetas Semánticas en HTML5</h1>
  </header>
  <nav>
    <a href="#">Inicio</a>
    <a href="#">Servicios</a>
    <a href="#">Contacto</a>
    <a href="#">Acerca De</a>
  </nav>
  <section>
    <h2>Sección 1</h2>
    <p>Información de la sección.</p>
    <aside>
      <p>Nombre del Autor</p>
    </aside>
  </section>
  <section>
    <h2>Sección 2</h2>
    <article>
      <h3>Artículo 1</h3>
    </article>
    <article>
      <h3>Artículo 2</h3>
    </article>
  </section>
  <footer>
    <h2>
      <a href="http://www.globalmentoring.com.mx"> GlobalMentoring.com.mx </a>
    </h2>
  </footer>
</template>

<script setup lang="ts"></script>

<style scoped>
header {
  color: #f72585;
  text-align: center;
  font-size: 20px;
}
nav {
  width: 20%;
  float: left;
}
nav a {
  background-color: #f71570;
  border-radius: 10px 0 10px 0;
  color: #fff;
  margin: 10px;
  padding: 10px;
  text-decoration: none;
  display: block;
}
section {
  float: right;
  width: 75%;
  color: #7209b7;
  border-radius: 5px;
  box-shadow: 1px 0 4px rgb(0, 0, 0, 0.2);
  margin-bottom: 15px;
  padding: 15px;
}
aside {
  float: right;
  width: 30%;
  padding: 5px;
  margin: 5px;
  font-style: italic;
  color: #4361ee;
  box-shadow: inset 5px 0 5px -5px #4895ef;
}
footer {
  clear: both;
  padding: 1px;
  text-align: center;
}
footer a {
  text-decoration: none;
}
</style>
