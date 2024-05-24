<script setup>
import { ref } from "vue";

const isVisible = ref(true);
</script>

<template>
  <div v-if="isVisible" class="visible">
    <p>If you can see this is because isVisible is true</p>
  </div>
</template>

<style>
.visible {
  display: flex;
  background-color: aqua;
  font-weight: bolder;
}
</style>
