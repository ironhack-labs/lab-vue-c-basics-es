<script setup>
import { ref } from "vue";
const cadena = ref("Prueba de mensaje");
</script>

<template>
  <h2>ITERACION 2:</h2>
  <h3>El resultado de la suma 2 + 2 es: {{ 2 + 2 }}</h3>

  <label for="cadena">Introduce el valor para la variable Cadena:</label>
  <input type="text" id="cadena" v-model="cadena" />

  <h4>El valor de la variable cadena es: {{ cadena }}</h4>
</template>
<style></style>
