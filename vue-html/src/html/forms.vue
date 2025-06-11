<template>
  <div>
    <h1>HMTL forms</h1>
    <form method="post" action="https://example.com/submit">
      <label for="nombre">Nombre:</label><br />
      <input type="text" id="nombre" name="nombre" placeholder="Escribe tu nombre" /><br />

      <label for="apellido">Apellido:</label><br />
      <input type="text" id="apellido" name="apellido" placeholder="Escribe tu apellido" /><br />
      
      <label for="email">Correo Electrónico:</label><br />
      <input
        type="email"
        id="email"
        name="email"
        placeholder="Escribe tu correo electrónico"
      /><br />
      
      <label for="telefono">Teléfono:</label><br />
      <input
        type="tel"
        id="telefono"
        name="telefono"
        placeholder="Escribe tu número de teléfono"
      /><br />

      <input type="submit" value="Enviar" />
    </form>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: auto;
}

label {
  margin-top: 10px;
}

input[type='text'],
input[type='email'],
input[type='tel'] {
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

input[type='submit'] {
  margin-top: 15px;
  padding: 10px;
  background-color: #28a745;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type='submit']:hover {
  background-color: #218838;
}
input[type='text']:focus,
input[type='email']:focus,
input[type='tel']:focus {
  border-color: #80bdff;
  outline: none;
}
h1 {
  text-align: center;
  color: #62f805;
    margin-bottom: 20px;
    font-size: 24px;
    font-weight: bold;
    font-family: Arial, sans-serif;
    text-transform: uppercase;
}
</style>
