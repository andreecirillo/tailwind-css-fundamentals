<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import PricingCard from './components/PricingCard.vue';
</script>
<template>
  <div>
    <NavBar/>
  </div>
  <div>
    <h1 class="text-3xl font-bold text-center m-5">Choose the best plan for your company</h1>
    <h2 class="text-1xl text-center m-5">We are sure that one of them will fit your business best.</h2>
  </div>
  <div class="grid lg:grid-cols-3 md:grid-cols-2 max-w-6xl mx-auto gap-6 p-4">
    <PricingCard price="25" :features="[
      'Unlimited Access to All Features',
      '24/7 Customer Support',
      'Customizable Dashboard',
      'Advance Analytics Tools',
      'Integration with Third-Party Services',
      'Secure Data Encryption'
    ]" name="Starter" description="Best option for personal use & for your next project." />
    <PricingCard price="50" :features="[
      'Multi-User Collaboration Tools',
      'Real-Time Data Backup',
      'Mobile App Access',
      'Custom Branding Options',
      'Automated Reporting System'
    ]" name="Plus" description="Great for small teams and anyone looking to scale." />
    <PricingCard price="150" :features="[
      'Priority Feature Updates',
      'Extended Data Storage Capacity',
      'Personalized User Experience',
      'In-Depth Training Materials',
      'Dedicated Account Manager'
    ]" name="Enterprise" description="Best for large scale uses and extended redistribution rights." />
  </div>
</template>