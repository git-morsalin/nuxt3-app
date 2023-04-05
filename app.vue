<template>
  <CustomInput v-model="message" /> {{ message }}
  <div>
    <!-- <NuxtWelcome /> -->
    <h1>Welcome to Nuxt from Me</h1>
    <div class="bg-red-200">box</div>
    <Hello helloData=""></Hello>
  </div>
</template>
<script setup>
  import { ref } from 'vue';
  let message = ref('hello whats up')
</script>
