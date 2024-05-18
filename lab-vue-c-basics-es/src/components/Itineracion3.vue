<script setup>
import {ref} from 'vue';

const publicaciones = [
      {
        titulo: 'Luces De Bohemia',
        ISBN: '842391307.',
        Valoración: '3-5'
      },
      {
        titulo: 'Crimen Y Castigo (Clasico)',
        ISBN: '8418008121',
        Valoración: '4-5'
      },
      {
        titulo: '100 años de soledad',
        ISBN: '8423919005',
        Valoración: '5-5'
      }
    ];

</script>


<template>

<h2>Publicaciones</h2>
<div>
    <ul>
        <li v-for="publicacion in publicaciones" :key="publicacion.titulo" >
            <h3>{{ publicacion.titulo }}</h3>
            <p>{{ publicacion.ISBN }}</p>
            <div>{{ publicacion.Valoración }}</div>
        </li>
    </ul>
</div>

</template>



<style scoped></style>