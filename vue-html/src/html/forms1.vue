<template>
  <div>
     <h1>Formularios en HTML</h1>
    <form>
        <label for="nombre">Nombre:</label><br/>
        <input type="text" id="nombre" name="nombre" 
            placeholder="Escribe tu nombre" required="true"/><br/>

        <label for="apellido">Apellido:</label><br/>
        <input type="text" id="apellido" name="apellido"
            placeholder="Escribe tu apellido" required="true"/><br/>

        <label for="email">Email:</label><br/>
        <input type="email" id="email" name="email"/><br/> 

        <label for="edad">Edad:</label><br/>
        <input type="number" id="edad" name="edad"/><br/>

        <label>Género</label><br/>
        <input type="radio" id="femenino" name="genero" value="femenino"/>
        <label for="femenino">Femenino</label><br/>
        <input type="radio" id="masculino" name="genero" value="masculino"/>
        <label for="masculino">Masculino</label><br/>     
        
        <label>Género Música Favorita</label><br/>
        <input type="checkbox" id="clasica" name="musica" value="clasica"/>
        <label for="clasica">Clásica</label><br/>
        <input type="checkbox" id="jazz" name="musica" value="jazz"/>
        <label for="jazz">Jazz</label><br/>
        
        <label for="autos">Marca Auto favorita:</label><br/>
        <select id="autos" name="autos">
            <option value="volvo">Volvo</option>
            <option value="bmw">BMW</option>
            <option value="audi" selected="true">Audi</option>
        </select><br/>

        <label for="comentario">Comentario:</label><br/>
        <textarea id="comentario" name="comentario" rows="2" cols="30"
        >Este es mi comentario    
        </textarea><br/>

        <br/>
        <input type="submit" value="Enviar"/>
        <input type="submit" formnovalidate value="Enviar sin validar"/>
    </form>
    
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
h1 {
  color: #333;
  font-size: 24px;
  margin-bottom: 20px;
    text-align: center;

}
form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #000000;
  border-radius: 5px;
  background-color: #daffb3;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;
  box-sizing: border-box;
  margin-top: 20px;
  margin-bottom: 20px;
  width: 100%;
}
label {
  margin-bottom: 5px;
  font-weight: bold;
}
input[type='text'],
input[type='email'],
input[type='number'],
input[type='radio'],
input[type='checkbox'],
input[type='submit'] {
  margin-bottom: 15px;
  padding: 8px;
  font-size: 16px;
}
</style>
