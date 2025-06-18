<template>
  <MyHeader 
  :cart="cart" 
  :guitarMain = "guitarMain" 
  @increment-cart="incrementCart" 
  @decrement-cart="decrementCart" 
  @delete-guitar="deleteGuitar"
  @delete-cart="deleteCart"
  @add-to-cart-main="addMainGuitarToCart"
  />

  <main class="container-xl mt-5">
    <h2 class="text-center">Our collection</h2>
    <div class="row mt-5">
      <blockGuitar
        v-for="guitar in guitars"
        :key="guitar.id"
        v-bind:guitar="guitar"
        @add-cart="addCart"
      />
    </div>
  </main>

  <MyFooter />
</template>

<script setup lang="ts">
import blockGuitar from './blockGuitar.vue';
import MyHeader from './myHeader.vue';
import MyFooter from './myFooter.vue';
import type { guitarData } from '../interfaces/guitarData.ts';

// Importing the guitar data from a mock database
import { db } from '../data/guitars.ts';
import { ref } from 'vue';

const guitars = ref(db);

const guitarMain = ref({});
guitarMain.value = db[3];

const cart = ref<guitarData[]>([]);

const addCart = (id: number, nombre: string, precio: number, imagen: string, cantidad: number) => {
  const existingGuitar = cart.value.findIndex((prod) => prod.id === id);
  if (existingGuitar >= 0) {
    if (typeof cart.value[existingGuitar].cantidad !== 'undefined') {
      cart.value[existingGuitar].cantidad++;
    }
  } else {
    const guitar = { id, nombre, precio, imagen, cantidad: 1 };
    cart.value.push(guitar);
  }
};

const incrementCart = (id: number) => {
  const guitar = cart.value.find((prod) => prod.id === id);
  if (guitar && typeof guitar.cantidad !== 'undefined') {
    guitar.cantidad++;
  }
};

const decrementCart = (id: number) => {
  const guitar = cart.value.find((prod) => prod.id === id);
  if (guitar && typeof guitar.cantidad !== 'undefined' && guitar.cantidad > 1) {
    guitar.cantidad--;
  }
};

const deleteGuitar = (id:number) => {
  const guitarIndex = cart.value.findIndex((prod) => prod.id === id);
  if (guitarIndex !== -1) {
    cart.value.splice(guitarIndex, 1);
  }
}

const deleteCart = () => {
  cart.value = [];
};

const addMainGuitarToCart = (guitar: guitarData) => {
  const existingGuitar = cart.value.findIndex((prod) => prod.id === guitar.id);
  if (existingGuitar >= 0) {
    if (typeof cart.value[existingGuitar].cantidad !== 'undefined') {
      cart.value[existingGuitar].cantidad++;
    }
  } else {
    cart.value.push({ ...guitar, cantidad: 1 });
  }
};


</script>

<style scoped></style>
