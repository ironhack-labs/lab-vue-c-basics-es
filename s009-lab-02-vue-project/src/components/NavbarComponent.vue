<template>
  <header>
    <nav>
      <img id="image-1" src="src/images/logo.png" alt="Logo Ironhack" />
      <h1>LAB | Fundaments of Vue.js (Composition API)</h1>
      <img id="image-2" src="src/images/burger.png" alt="Burger Menu" />
    </nav>
  </header>
</template>

<script setup></script>

<style scoped>
nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 30px 20px;
}

nav h1 {
  font-weight: 400;
}

#image-1 {
  width: 35px;
  height: 38px;
}

#image-2 {
  width: 22px;
  height: 20px;
}
</style>
