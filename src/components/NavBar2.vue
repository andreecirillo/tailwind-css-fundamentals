<script setup lang="ts">
import { ref } from 'vue';
const active = ref(false);
const mobileActive = ref(false);
</script>
<template>
    <header class="bg-gray-800 p-2 flex items-center justify-between text-white relative">
        
        <div class="flex items-center">
            <button class="w-8 flex flex-col gap-1 sm:hidden outline outline-white p-2 rounded bg-gray-700"
            @click="$event => mobileActive = !mobileActive">
            <span class="block h-[2px] bg-white w-full"></span>
            <span class="block h-[2px] bg-white w-full"></span>
            <span class="block h-[2px] bg-white w-full"></span>
        </button>
            <img src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500" alt="TailwindUI"
                class="w16 h-16 ml-3 mr-3" />
            <ul class="gap-1 top-full absolute flex flex-col sm:static sm:flex-row text-left left-0 bg-gray-800 w-full p-2"
                v-if="mobileActive">
                <li class="bg-gray-900 hover:bg-gray-500 px-2 py-1 rounded cursor:pointer text-gray-300">Dashboard</li>
                <li class="hover:bg-gray-500 px-2 py-1 rounded cursor:pointer text-gray-300">Team</li>
                <li class="hover:bg-gray-500 px-2 py-1 rounded cursor:pointer text-gray-300">Projects</li>
                <li class="hover:bg-gray-500 px-2 py-1 rounded cursor:pointer text-gray-300">Calendar</li>
            </ul>
        </div>
        <div class="flex items-center gap-2">
            <svg class="h-6 w-6 " fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round"
                    d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0">
                </path>
            </svg>
            <div class="relative">
                <button @click="$event => active = !active">
                    <img class="w-10 h-10 rounded-full ring-white ring-2 ring-offset-2 ring-offset-gray-700"
                        src="https://avatars.githubusercontent.com/u/57644030?v=4" alt="André Cirillo" />
                </button>
                <ul v-if="active"
                    class="absolute top-full right-0 bg-white text-gray-800 p2 rounded min-w-[175px] flex flex-col gap-2">
                    <li class="p-2 hover:bg-gray-100 rounded">Your Profile</li>
                    <li class="p-2 hover:bg-gray-100 rounded">Settings</li>
                    <li class="p-2 hover:bg-gray-100 rounded">Signout</li>
                </ul>
            </div>
        </div>
    </header>
</template>
