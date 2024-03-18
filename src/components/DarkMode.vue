<script setup language="ts">
import AppInput from './AppInput.vue';
import AppButton from './AppButton.vue';
import TheMainNav from './TheMainNav.vue';
import { useDark } from "@vueuse/core";
const isDark = useDark();
</script>
<template>
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
</template>