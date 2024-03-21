<script setup lang="ts">
import { ref } from "vue";

const showMenu = ref(false);
const showNav = ref(false);

const toggleMenu = () => {
    showMenu.value = !showMenu.value;
};

const toggleNav = () => {
    showNav.value = !showNav.value;
};
</script>
<template>
    <div class="flex flex-row justify-around bg-gray-700 p-5">
        <div class="md:hidden">
            <button class="block" @click="toggleNav">
                <img class="h-5 w-5" src="/src/assets/menu.png" />
            </button>
            <div :class="showNav ? 'block' : 'hidden'"
                class="absolute left-1 mt-2 flex flex-col rounded-lg bg-white p-2">
                <a class="menuItem" href="#">Dashboard</a>
                <a class="menuItem" href="#">Team</a>
                <a class="menuItem" href="#">Projects</a>
                <a class="menuItem" href="#">Calendar</a>
            </div>
        </div>
        <div>
            <img class="h-6 w-8" src="/src/assets/tailwind.png" />
        </div>
        <div class="ml-3 hidden flex-row md:flex">
            <a class="navItem" href="#">Dashboard</a>
            <a class="navItem" href="#">Team</a>
            <a class="navItem" href="#">Projects</a>
            <a class="navItem" href="#">Calendar</a>
        </div>
        <div>
            <button class="block" @click="toggleMenu">
                <img class="h-10 w-10 rounded-full" src="/src/assets/user.jpg" />
            </button>
            <div :class="showMenu ? 'block' : 'hidden'"
                class="absolute right-1 mt-2 flex flex-col rounded-lg bg-white p-2">
                <a class="menuItem" href="#">Your Profile</a>
                <a class="menuItem" href="#">Settings</a>
                <a class="menuItem" href="#">Sign Out</a>
            </div>
        </div>
    </div>
</template>
<style scoped>
a.navItem {
    @apply mr-5 block p-2 text-white hover:rounded-lg hover:bg-gray-600;
}

a.menuItem {
    @apply block p-1 text-black hover:rounded-lg hover:bg-gray-100;
}
</style>
