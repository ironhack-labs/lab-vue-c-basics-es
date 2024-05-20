<script setup>
import { computed, ref } from "vue";

let name = ref("Matias");
const getName = () => {
  return name.value;
};

let showElement = ref(true);

const showElementActive = () => {
  showElement.value = !showElement.value;
};

const buttonText = computed(() => {
  return showElement.value ? "Ocultar Contenido" : "Mostrar Contenido";
});
</script>

<template>
  <h1>NavbarComponent</h1>
  <h2>Interación 2</h2>
  <p>La suma de 2 + 2 es: {{ 2 + 2 }}</p>
  <p>El nombre conseguido a traves de una función es: {{ getName(name) }}</p>

  <h2>Interación 3</h2>
  <button @click="showElementActive">{{ buttonText }}</button>
  <p v-if="showElement">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis,
    harum?
  </p>
  <hr />
</template>

<style></style>

