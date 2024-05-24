<script setup>
import { ref } from "vue";

const posts = ref([
  {
    title: "Summer",
    description: "Light and fun",
    content: 278889,
  },
  {
    title: "Winter",
    description: "Húmid and cold",
    content: 959626,
  },
  {
    title: "Spring",
    description: "Flowery and lovely",
    content: 979795,
  },
]);
</script>

<template>
  <ul>
    <li v-for="post in posts" :key="post.content">
      <h3>{{ post.title }}</h3>
      <p>{{ post.description }}</p>
      <p>{{ post.content }}</p>
    </li>
  </ul>
</template>

<style></style>
