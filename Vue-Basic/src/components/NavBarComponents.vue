<script setup>
    import { ref } from 'vue';
    
    // iteracion 2
    const cadena = ref('Hola soy una cadena reactiva');
    const cadenaReactiva = () => {
        return cadena.value;
    }
// iteracion 3
const expresionBoleam = ref(true);

</script>


<template>
    <!-- iteracion 2 -->
    <h1>{{ 2 + 2 }}</h1>
    <p>{{ cadenaReactiva() }}</p>

    <!-- iteracion 3 -->
    <p v-if="expresionBoleam">Si es true, mostrare esta linea.</p>
</template>

<style></style>