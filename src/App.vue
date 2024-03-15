<script setup language="ts">
import AppInput from './components/AppInput.vue';
import AppButton from './components/AppButton.vue';
import TheMainNav from './components/TheMainNav.vue';
import { useDark } from "@vueuse/core";

const isDark = useDark();
</script>
<template>
  <div class="m-10">
    <input type="checkbox" v-model="isDark"/>Dark Mode
    <TheMainNav />
    <form action="">
      <label></label>
      <AppInput label="Username" />
      <AppButton>Submit</AppButton>
    </form>
    <p class="first-letter:text-5xl selection:bg-blue-500 selection:text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis maxime nisi beatae, assumenda voluptatibus sit consectetur ab quod eius possimus culpa ratione? Saepe, culpa delectus. Asperiores illum ut eveniet vel?</p>
    <ul class="list-disc marker:text-green-500 marker:text-2xl">
      <li>Vue.js</li>
      <li>React</li>
      <li>Svelte</li>
      <li>Solid</li>      
    </ul>
  </div>
</template>