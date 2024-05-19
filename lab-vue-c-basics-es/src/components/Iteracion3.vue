<script setup>
import { ref } from "vue";

const MostrarSi = ref(false);
const MostrarShow = ref(false);

const toogleMostarSi = () => {
  MostrarSi.value = !MostrarSi.value;
};

const toogleMostarShow = () => {
  MostrarShow.value = !MostrarShow.value;
};
</script>
<template>
  <h2>ITERACION 3:</h2>
  <div>
    <h5 v-if="MostrarSi">Hola, me estoy mostrando</h5>
    <button @click="toogleMostarSi">Mostrar texto if</button>
  </div>
  <div>
    <h5 v-if="MostrarShow">Hola, me estoy "SHOWstrando"</h5>
    <button @click="toogleMostarShow">Mostrar texto show</button>
  </div>
</template>
<style></style>
