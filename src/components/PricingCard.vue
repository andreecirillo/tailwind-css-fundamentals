<script setup lang="ts">
defineProps<{
    price: number;
    features: string[];
    name: string;
    description: string;
}>();
</script>
<template>
    <div class="dark:bg-gray-800 p-4 border rounded-lg text-center flex flex-col justify-between">
        <div>
            <h3 class="font-bold text-xl mb-4">{{ name }}</h3>
            <p class="text-gray-500 mb-4">{{ description }}</p>
            <div>
                <span class="text-4xl font-bold inline-block mr-2">${{ price }}</span>
                <span class="text-gray-500">/month</span>
            </div>
            <ul role="list" class="text-left mt-4">
                <li class="flex mb-3" v-for="feature in features" :key="feature">
                    <svg class="w-5 h-5 text-green-500 mr-2" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd"
                            d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                            clip-rule="evenodd"></path>
                    </svg>
                    <span>{{ feature }}</span>
                </li>
            </ul>
        </div>
        <a class="bg-blue-600 hover:bg-blue-700 text-white m-5 px-4 py-2 rounded block" href="#">Get started</a>
    </div>
</template>