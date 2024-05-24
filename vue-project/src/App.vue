<script setup>
import NavbarComponent from "./components/NavbarComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import { ref } from "vue";

const firstName = ref("Joana");
const lastName = ref("Silva");
function fullMessage() {
  return `Hello ${firstName.value} ${lastName.value}`;
}
</script>

<template>
  <NavbarComponent></NavbarComponent>
  <FooterComponent></FooterComponent>
  <div>
    <p>{{ 5 + 8 }}</p>
    <p>{{ fullMessage() }}</p>
  </div>
</template>

<style></style>
