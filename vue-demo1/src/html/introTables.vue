<template>
  <div>
    <table border="1">
      <caption>
        Table of Users
      </caption>
      <tr>
        <th>Name</th>
        <th>Surname</th>
        <th>Email</th>
      </tr>
      <tr>
        <td>Alfi</td>
        <td>Sun</td>
        <td>panchopistolas@mail.com</td>
      </tr>
      <tr>
        <td>Mery</td>
        <td>Sunflower</td>
        <td>cheetito@mail.com</td>
      </tr>
    </table>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
table,
th,
td {
  border: 1px solid black;
  border-spacing: 0;
  border-radius: 5px;
  text-align: center;
  font-family: 'Courier New', Courier, monospace;
  font-size: 16px;
  background-color: rgb(202, 254, 195);
  color: rgb(0, 0, 0);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 50px;
  border-collapse: collapse;
  padding: 5px;
}
caption{
    color: #000000;
    font-family: 'Trocchi', serif;  
    font-size: 25px;
    line-height: 70px;
    font-weight: bold;
    text-align: center;
    margin-bottom: 20px;
    text-transform: uppercase;
    letter-spacing: 2px;
    background-color: #e8e8e8;
    padding: 10px;
    border-radius: 10px;
}
</style>
