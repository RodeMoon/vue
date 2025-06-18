<template>
  <header class="py-5 header">
    <div class="container-xl">
      <div class="row justify-content-center justify-content-md-between">
        <div class="col-8 col-md-3">
          <a href="index.html">
            <img class="img-fluid" src="../../public/img/logo.svg" alt="imagen logo" />
          </a>
        </div>
        <nav class="col-md-6 a mt-5 d-flex align-items-start justify-content-end">
          <div class="carrito">
            <img class="img-fluid" src="../../public/img/carrito.png" alt="imagen carrito" />

            <div id="carrito" class="bg-white p-3">
              <p v-if="cart.length === 0" class="text-center">The cart is empty</p>
              <div v-else>
                <table class="w-100 table">
                  <thead>
                    <tr>
                      <th>Imagen</th>
                      <th>Nombre</th>
                      <th>Precio</th>
                      <th>Cantidad</th>
                      <th></th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="guitar in cart" :key="guitar.id">
                      <td>
                        <img
                          class="img-fluid"
                          v-bind:src="'/img/' + guitar.imagen + '.jpg'"
                          v-bind:alt="'image ' + guitar.nombre"
                        />
                      </td>
                      <td>{{ guitar.nombre }}</td>
                      <td class="fw-bold">{{ guitar.precio }}</td>
                      <td class="flex align-items-start gap-4">
                        <button
                          type="button"
                          class="btn btn-dark"
                          @click="$emit('decrementCart', guitar.id)"
                        >
                          -
                        </button>
                        {{ guitar.cantidad }}
                        <button
                          type="button"
                          class="btn btn-dark"
                          @click="$emit('incrementCart', guitar.id)"
                        >
                          +
                        </button>
                      </td>
                      <td>
                        <button class="btn btn-danger" type="button"
                        @click="$emit('deleteGuitar', guitar.id)">
                        X</button>
                      </td>
                    </tr>
                  </tbody>
                </table>

                <p class="text-end">
                  Total: <span class="fw-bold">${{ totalCost }}</span>
                </p>
                <button class="btn btn-dark w-100 mt-3 p-2"
                @click="$emit('deleteCart')"
                >Empty cart</button>
              </div>
            </div>
          </div>
        </nav>
      </div>
      <!--.row-->

      <div class="row mt-5">
        <div class="col-md-6 text-center text-md-start pt-5">
          <h1 class="display-2 fw-bold">Model {{ guitarMain.nombre }}</h1>
          <p class="mt-5 fs-5 text-white">
            {{ guitarMain.descripcion }}
          </p>
          <p class="text-primary fs-1 fw-black">${{ guitarMain.precio }}</p>
          <button type="button" class="btn fs-4 bg-primary text-white py-2 px-5"
          @click="$emit('addToCartMain', guitarMain)"
          >
            Add to the cart
          </button>
        </div>
      </div>
    </div>

    <img class="header-guitarra" src="../../public/img/header_guitarra.png" alt="imagen header" />
  </header>
</template>

<script setup lang="ts">
import type { guitarData } from '@/interfaces/guitarData';
import { computed } from 'vue';

const props = defineProps({
  cart: {
    type: Array,
    required: true,
  },
  guitarMain: {
    type: Object,
    required: true,
  },
});

defineEmits<{
  incrementCart: [id: number];
  decrementCart: [id: number];
  deleteGuitar: [id: number];
  deleteCart: [];
  addToCartMain: [guitar: guitarData];
}>();

const totalCost = computed(() => {
  return props.cart.reduce((total: number, cart) => total + cart.precio * cart.cantidad, 0);
});
</script>

<style scoped></style>
