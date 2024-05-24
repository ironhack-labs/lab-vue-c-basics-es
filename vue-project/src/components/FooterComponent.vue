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

const isActive = ref(false);

function toggleActiveClass() {
  isActive.value = !isActive.value;
}
</script>

<template>
  <div :class="{ active: isActive }">
    This text changes appearance based on isActive.
  </div>
  <button @click="toggleActiveClass">Toggle Active Class</button>
  <ul>
    <li v-for="post in posts" :key="post.content">
      <h3>{{ post.title }}</h3>
      <p>{{ post.description }}</p>
      <p>{{ post.content }}</p>
    </li>
  </ul>
</template>

<style>
.active{
  color: green;
  font-weight: bold;
}</style>
