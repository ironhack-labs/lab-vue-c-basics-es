<script setup>
import NavbarComponents from './components/NavbarComponents.vue';
import FooterComponent from "./components/FooterComponent.vue";
import { ref } from "vue";
import { reactive, computed } from 'vue'

//  iteracion 2 

const user = reactive({
  name: {
    first: 'David',
    last: 'Bigas'
  },
  age: 27
})

const isEighteen = computed(()=>{
  return user.age > 18 ? 'yes' : 'No'
})

// iteracion 3
const myBoolean = true

// iteracion 4 v-for

const posts = [{
  title: 'Great Barrier Reef',
  description: 'One of the biggest mysteries of the Great Barrier Reef',
  content: 'One of the biggest mysteries of the Great Barrier Reef are blue holes that can give researchers a rare look at ocean life and how we can protect it. Dive in to see how researchers are using @GoogleMaps to locate and learn from these sinkholes'
},
{
  title: 'Tonys Chocolonely',
  description: 'New store',
  content: 'We have got very exciting news.. Tony Chocolonely Chocolate Bar is open! This seriously crazy Chocolate Bar is a dream coming true for every choco fan. In the Bar you will be enjoying the most crazy delicious choco-creations, all made from Tonys chocolate (made with fully traceable cocoa beans from West Africa), whilst at the same time learning more about Tonys serious mission: to make 100% slave free the norm in chocolate. See you in the Bar?'
},
{
  title: 'Social Media Examiner',
  description: 'Share your expertise',
  content: 'NEW: Social Media Marketing Strategy: How to Thrive in a Changing World'
}]

// bonus

const colorChange = ref(false)
const toggleColor = ()=>{
  colorChange.value = !colorChange.value
}
</script>

<template>

<!-- iteracion 1 componentes hecho -->

  <NavbarComponents></NavbarComponents>

<!-- iteracion 2 - segunda parte falta  -->

  <h2>{{ 2 + 2 }}</h2>
  <h3>Is the user 18 or older?</h3>
  <span>{{ isEighteen }}</span>
  

<!-- iteracion 3 renderizado condicional hecho-->

  <h1 v-if="myBoolean">My Boolean is true and is showing</h1>
  <h1 v-show ="myBoolean">My Boolean is true and is showing</h1>

<!-- iteracion 4 v-for -->

<ul>
  <li v-for = 'post in posts'>
    <h2>{{ post.title }}</h2>
    <h3>{{ post.description }}</h3>
    <p>{{ post.content }}</p> 
  </li>
</ul>
<br>

<p :class="colorChange ? 'highlight' : ''">This text is going to show in another color</p>

<button @click = "toggleColor">this button is going to change text color</button>

<br>

  <FooterComponent></FooterComponent>

</template>

<style scoped>

.highlight { 
  background-color: lightblue;
  color: red;
}
</style>