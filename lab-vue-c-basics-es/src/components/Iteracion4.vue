<script setup>
import { ref } from "vue";

const publicaciones = [
  {
    ID: "001",
    Titulo: "Hola!",
    Descripcion: "Revista",
    Contenido: "Cotilleo",
  },
  {
    ID: "002",
    Titulo: "Don Quijote de la Mancha",
    Descripcion: "Libro",
    Contenido: "Novela de caballería",
  },
  {
    ID: "003",
    Titulo: "One Piece",
    Descripcion: "Manga",
    Contenido: "Shonen",
  },
];
</script>

<template>
  <h2>ITERACION 4</h2>
  <h3>Estas son las publicaciones:</h3>
  <div>
    <ul>
      <li v-for="publicacion in publicaciones" :key="publicacion.ID">
        <h5>Título: {{ publicacion.Titulo }}</h5>
        <p>Descripción: {{ publicacion.Descripcion }}</p>
        <div>Contenido: {{ publicacion.Contenido }}</div>
      </li>
    </ul>
  </div>
</template>

<style></style>
