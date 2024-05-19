<script setup>
import NavBarComponents from './components/NavBarComponents.vue';
import FoooterComponents from './components/FoooterComponents.vue';
import { ref } from 'vue';
// iteracion 2
const cadena = ref('Hola soy una cadena reactiva');
const cadenaReactiva = () => {
  return cadena.value;
}
// iteracion 3
const expresionBoleam = ref(true);

// iteracion 4
const publicacion = ref([
   {
    id : 1,
    titulo: "American paint 1",
    descripcion: "Cuatro adolescentes se comprometen a perder su virginidad antes de acabar su etapa en el instituto y acuerdan hacerlo antes del baile de fin de curso.",
    contenido: "Pelicula de genero comedia."
   },
   {
    id: 2,
    titulo: "American paint 2",
    descripcion: " Un año después de la accidentada fiesta de fin de curso en el instituto, la pandilla decide reunirse en una casa de verano en la playa.",
    contenido: "Pelicula de genero comedia."
   },
   {
    id: 3,
    titulo: "American paint 3",
    descripcion: "Jim y Michelle están a punto de casarse y, cómo no, el encargado de organizar la despedida de soltero de Jim es el alocado de Stifler.",
    contenido: "Pelicula de genero comedia."
   }
   ]);

  //  iteracion 5
const cambiarColor = ref("Cambiare de color al pulsar el boton.");
const isFondo = ref(false);

const cambiarFondo = () =>{
  isFondo.value = !isFondo.value; //Alterna el valor de isFondo entre true y false
  cambiarColor.value = isFondo.value ? 'Fondo cambiado' :  'Cambiare de color al pulsar el boton';
}

</script>

<template>

  <NavBarComponents />
  <FoooterComponents />
  <!-- iteracion 2 -->
  <h1>{{ 2 + 2 }}</h1>
  <p>{{ cadenaReactiva() }}</p>

  <!-- iteracion 3 -->
  <p v-if="expresionBoleam">Si es true, mostrare esta linea.</p>

  <!-- iteracion 4 -->
  <ul>
    <li v-for="publicaciones in publicacion" :key="publicaciones.id">
    <h3>{{ publicaciones.titulo }}</h3>
    <p>{{ publicaciones.descripcion }}</p>
    <p>{{ publicaciones.contenido }}</p>
    </li>
  </ul>

  <!-- iteracion 5 -->
  <button @click="cambiarFondo">Cambiar de color </button>
  <h1 :class="{fondo : isFondo}">{{ cambiarColor }}</h1>

</template>

<style>
.fondo{
  background-color: brown;
  color: aliceblue;
}
</style>