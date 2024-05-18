<script setup>
import {ref} from "vue";

const isShow = ref(true)



const show = ref(true)


</script>
<template>
    <div v-if="isShow">
        <h2>v-if </h2>
         <p >Voy a utilizar v-if </p>
    </div>
    <div v-else="isShow">
        <h2>v-if </h2>
         <p >no puedes utilizar v-if </p>
    </div>
    <div>
        <h2>v-show </h2>
         <p v-show="show">Vou a utilizar v-show </p>
    </div>

</template>
<style scoped></style>