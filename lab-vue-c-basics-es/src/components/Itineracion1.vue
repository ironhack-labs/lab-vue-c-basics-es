<script setup>
import {ref} from "vue";

const nombre = ref("");


const isBackGround = ref(false);

const toggleBackGround = () => {
  isBackGround.value = !isBackGround.value;
};

</script>
<template>
  <div  >
    <h1>{{ 2 + 2 }}</h1>
    
    <div>
      <h2>{{ nombre }}</h2>
      <label for="nombre" >Cadena string</label>
      <input type="text" id="nombre" v-model="nombre">

      <p :class="isBackGround ? 'background' : ''" >Prueba background-color</p>
      <button @click="toggleBackGround" >background</button>
    </div>
  </div>


</template>
<style scoped>
.background {
  background-color: black;
  color: yellow;

  
}
</style>