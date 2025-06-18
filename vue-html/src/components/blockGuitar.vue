<template>
  <div class="col-md-6 col-lg-4 my-4 row align-items-center">
    <div class="col-4">
      <img
        class="img-fluid"
        v-bind:src="'/img/' + guitar.imagen + '.jpg'"
        v-bind:alt="'image ' + guitar.nombre"
      />
    </div>
    <div class="col-8">
      <h3 class="text-black fs-4 fw-bold text-uppercase">{{ guitar.nombre }}</h3>
      <p>
        {{ guitar.descripcion }}
      </p>
      <p class="fw-black text-primary fs-3">${{ guitar.precio }}</p>
      <button
        type="button"
        class="btn btn-dark w-100"
        @click="
          $emit('addCart', guitar.id, guitar.nombre, guitar.precio, guitar.imagen, guitar.cantidad)
        "
      >
        Add to the cart
      </button>
    </div>
  </div>
  <!-- FIN GUITARRA -->
</template>

<script setup lang="ts">
defineEmits<{
  addCart: [id: number, nombre: string, precio: number, imagen: string, cantidad: number];
}>();

defineProps({
  guitar: {
    type: Object,
    required: true,
  },
});
</script>

<style scoped></style>
