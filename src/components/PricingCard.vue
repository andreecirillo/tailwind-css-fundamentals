<script setup lang="ts">
defineProps<{
    price: number;
    features: string[];
    name: string;
    description: string;
}>();
</script>
<template>
    <div class="border rounded">
        <div>
            <h3 class="font-medium text-2xl text-center m-5">{{ name }}</h3>
            <p class="text-center m-5">{{ description }}</p>
            <div class="bg-[url('/checkmark.png')] text-center m-5">
                <span class="font-medium text-5xl">${{ price }}</span>
                <span>/month</span>
            </div>
            <ul role="list" class="list-disc marker:text-green-500 m-5 p-5">
                <li class="space-h-5" v-for="feature in features" :key="feature">
                    <span>{{ feature }}</span>
                </li>
            </ul>
        </div>
        <a class="bg-blue-500 hover:bg-blue-600 text-white text-center m-5 p-1 rounded block" href="#">Get started</a>
    </div>
</template>