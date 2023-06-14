<script setup>
import NavbarComponent from "./components/NavbarComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";

import { ref, computed } from "vue";

const result = ref(2 + 2);
const name = ref("Nico");
const surname = ref("D'Alessandro");
const myBoolean = ref(true);
const isActive = ref(true);
const posts = ref([
  {
    id: 1,
    title: "Introduction to Vue.js",
    description: "Learn the basics of Vue.js framework",
    content:
      "Vue.js is a progressive JavaScript framework for building interactive user interfaces. It is designed to be incrementally adoptable, which means you can start using Vue.js for small sections of your project and gradually scale it up to a full-fledged single-page application. With its simple and intuitive syntax, Vue.js makes it easy to create dynamic and reactive components. It provides features such as declarative rendering, component-based architecture, reactivity system, and a powerful template system. Whether you are a beginner or an experienced developer, Vue.js offers great flexibility and performance, making it a popular choice for web development.",
  },
  {
    id: 2,
    title: "Building Dynamic Web Applications with Vue",
    description: "Explore how to build interactive web apps with Vue.js",
    content:
      "Building dynamic web applications has never been easier with Vue.js. With its component-based architecture, you can create reusable and modular UI components that can be combined to build complex user interfaces. Vue.js provides a powerful reactivity system, allowing you to easily update and manage the state of your application. Whether you need to handle form input, make asynchronous requests, or implement real-time updates, Vue.js has you covered. Its seamless integration with other libraries and tools, such as Vue Router and Vuex, further enhances the development experience. Start building your next web app with Vue.js and unleash its full potential.",
  },
  {
    id: 3,
    title: "Mastering Vue Router for Single-Page Applications",
    description: "Get in-depth knowledge of Vue Router",
    content:
      "Vue Router is a key feature of Vue.js that enables you to build single-page applications with ease. It provides a powerful routing system that allows you to define your application's navigation and handle dynamic routing. With Vue Router, you can create multiple routes, nested routes, and even lazy-load components to optimize the performance of your application. Additionally, Vue Router supports features like route parameters, query parameters, and navigation guards, giving you fine-grained control over your application's routing behavior. Mastering Vue Router will unlock the full potential of your Vue.js applications and take your web development skills to the next level.",
  },
]);

const generateName = computed(() => {
  return `I am ${name.value} ${surname.value}`;
});

const changeVisibility = () => {
  isActive.value ? (isActive.value = false) : (isActive.value = true);
};
</script>

<template>
  <body>
    <NavbarComponent />

    <section id="iteration-2">
      <h2>
        Iteration 2 | Display the result of a JavaScript operation in the HTML
        of a component
      </h2>
      <div class="iteration-section">
        <div class="section-title">
          <h3>A - Display the result of a JavaScript operation in the HTML</h3>
        </div>

        <div class="section-operation">
          <p>The result is {{ result }}</p>
        </div>
      </div>

      <div class="iteration-section">
        <div class="section-title">
          <h3>
            B - Print a string in the Vue template using a function and data
            stored in reactive variables
          </h3>
        </div>

        <div class="section-operation">
          <p>Hello, {{ generateName }}</p>
        </div>
      </div>
    </section>

    <section id="iteration-3">
      <h2>
        Iteration 3 | Display an element only if a specific property is set to
        <span>true</span>
      </h2>
      <div class="section-operation">
        <p v-if="myBoolean">
          This is being displayed because myBoolean is
          <span>{{ myBoolean }}</span>
        </p>
      </div>
    </section>

    <section id="iteration-4">
      <h2>Iteration 4 | Display a list of items stored within a component</h2>
      <div class="section-operation">
        <ul>
          <li v-for="post in posts" :key="post.id">
            <h4>{{ post.title }}</h4>
            <p>{{ post.description }}</p>
            <p>{{ post.content }}</p>
          </li>
        </ul>
      </div>
    </section>

    <section id="iteration-4">
      <h2>
        Iteration 5 | Bonus | Change the background color of an element when a
        button is clicked
      </h2>
      <div class="section-operation">
        <button @click="changeVisibility">Try me</button>
        <div class="text-container">
          <p :class="{ active: isActive, notActive: !isActive }">
            I'm a Chamaeleon
          </p>
        </div>
      </div>
    </section>

    <FooterComponent />
  </body>
</template>

<style scoped>
* {
  font-weight: 100;
  font-family: "Inter", sans-serif;
  color: #2b2f30;
}

section h2 {
  background-color: #39b983;
  padding: 10px;
}

section .section-title {
  margin-left: 10px;
}

section .section-operation {
  margin-left: 20px;
  background-color: lightgray;
  padding: 1px;
  padding-left: 10px;
}

section .section-operation span,
section h2 span {
  background-color: #2b2f30;
  font-family: "Courier New", Courier, monospace;
  color: white;
}

section .section-operation ul li h4 {
  font-weight: 600;
}

section .section-operation ul li p:first-of-type {
  font-style: italic;
}

section .section-operation .active {
  visibility: hidden;
}
section .section-operation .notActive {
  background-color: #2b2f30;
  color: white;
}
section .section-operation .text-container {
  display: inline-block;
  padding: 5px;
  margin-left: 10px;
}

section .section-operation .text-container p {
  padding: 5px;
  border-radius: 5px;
}

section .section-operation button {
  padding: 5px;
  background-color: #39b983;
  color: #2b2f30;
  border: none;
}

section .section-operation button:hover {
  background-color: #2b2f30;
  color: white;
}
</style>
