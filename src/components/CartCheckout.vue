<script setup lang="ts">
import CartCheckoutLeft from "./CartCheckoutLeft.vue"
import CartCheckoutRight from "./CartCheckoutRight.vue"
import CartCheckoutShadow from "./CartCheckoutShadow.vue"
</script>
<template>
    <div class="relative bg-[#d9d9d9]">
        <div class="rounded-2xl overflow-hidden bg-[323239] border-white border-2 grid grid-cols-9 relative z-10">
            <CartCheckoutLeft/>
            <CartCheckoutRight/>
        </div>
        <CartCheckoutShadow/>
    </div>
</template>