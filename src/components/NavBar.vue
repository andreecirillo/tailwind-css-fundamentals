<script setup lang="ts">
import { ref } from 'vue'

const showMenu = ref(false)
const showNav = ref(false)

const toggleMenu = () => {
    showMenu.value = !showMenu.value
}

const toggleNav = () => {
    showNav.value = !showNav.value
}
</script>
<template>
    <div class="bg-gray-700 flex flex-row justify-around p-5">
        <div class="md:hidden">
            <button class="block" @click="toggleNav">
                <img class="w-5 h-5" src="/src/assets/menu.png" />
            </button>
            <div :class="showNav ? 'block' : 'hidden'"
                class="bg-white mt-2 rounded-lg p-2 flex flex-col absolute left-1">
                <a class="menuItem" href="#">Dashboard</a>
                <a class="menuItem" href="#">Team</a>
                <a class="menuItem" href="#">Projects</a>
                <a class="menuItem" href="#">Calendar</a>
            </div>
        </div>
        <div>
            <img class="w-8 h-6" src="/src/assets/tailwind.png" />
        </div>
        <div class="ml-3 hidden md:flex flex-row">
            <a class="navItem" href="#">Dashboard</a>
            <a class="navItem" href="#">Team</a>
            <a class="navItem" href="#">Projects</a>
            <a class="navItem" href="#">Calendar</a>
        </div>
        <div>
            <button class="block" @click="toggleMenu">
                <img class="w-10 h-10 rounded-full" src="/src/assets/user.jpg" />
            </button>
            <div :class="showMenu ? 'block' : 'hidden'"
                class="bg-white mt-2 rounded-lg p-2 flex flex-col absolute right-1">
                <a class="menuItem" href="#">Your Profile</a>
                <a class="menuItem" href="#">Settings</a>
                <a class="menuItem" href="#">Sign Out</a>
            </div>
        </div>
    </div>
</template>
<style scoped>
a.navItem {
    @apply mr-5 p-2 text-white hover:bg-gray-600 hover:rounded-lg block;
}

a.menuItem {
    @apply p-1 text-black hover:bg-gray-100 hover:rounded-lg block;
}
</style>