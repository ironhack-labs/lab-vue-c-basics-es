<script setup>
import { computed, ref } from "vue";

const publicaciones = ref([
  {
    id: 1,
    titulo: "La Evolución de la Tecnología",
    descripcion:
      "Un vistazo a cómo la tecnología ha transformado nuestras vidas en las últimas décadas.",
    contenido:
      "Desde la invención del internet hasta los avances en inteligencia artificial, la tecnología ha revolucionado todos los aspectos de nuestra vida diaria. Este artículo explora los hitos más significativos y cómo han impactado la sociedad moderna.",
  },
  {
    id: 2,
    titulo: "El Futuro del Trabajo",
    descripcion:
      "Predicciones sobre cómo será el entorno laboral en los próximos años.",
    contenido:
      "Con la automatización y la digitalización, el mundo laboral está cambiando rápidamente. Este artículo analiza las tendencias emergentes, como el teletrabajo y la economía gig, y cómo se están redefiniendo las carreras tradicionales.",
  },
  {
    id: 3,
    titulo: "La Importancia de la Salud Mental",
    descripcion:
      "Comprender y abordar la salud mental en la sociedad contemporánea.",
    contenido:
      "La salud mental ha ganado reconocimiento como un componente crucial del bienestar general. En este artículo, se discuten las diversas estrategias para mejorar la salud mental, desde la terapia hasta el autocuidado, y la importancia de desestigmatizar las enfermedades mentales.",
  },
]);

const backgroundOn = ref(false);

const toogleBackground = () => {
  backgroundOn.value = !backgroundOn.value;
};

const buttonColor = computed(() => {
  return backgroundOn.value ? "Background Color Off" : "Background Color On";
});
</script>

<template>
  <h1>FooterComponent</h1>
  <h2>Iteración 4</h2>
  <h2>Publicaciones</h2>
  <ul>
    <li v-for="publicacion in publicaciones" :key="publicacion.id">
      <h2>{{ publicacion.titulo }}</h2>
      <h3>{{ publicacion.descripcion }}</h3>
      <p>{{ publicacion.contenido }}</p>
    </li>
  </ul>
  <br />
  <h2>Iteración 5</h2>
  <button @click="toogleBackground">{{ buttonColor }}</button>
  <p :class="backgroundOn ? 'back-color' : ''">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium aperiam
    sunt, officiis odit repudiandae reprehenderit a corporis necessitatibus.
    Ipsa ipsam repellendus magnam id iusto reiciendis dolor neque mollitia
    fugiat, ducimus adipisci dolore cumque eligendi error cum quam alias ab iste
    temporibus animi accusamus reprehenderit corrupti nihil! Quidem saepe
    reprehenderit cumque!
  </p>
</template>

<style>
.back-color {
  background-color: cornflowerblue;
}
</style>
