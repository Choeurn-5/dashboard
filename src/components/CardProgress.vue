<template>
    <div class="card bg-white shadow p-4 rounded-lg mb-4">
      <h2 class="text-gray-700 font-semibold">{{ title }}</h2>
      <div v-for="(item, index) in progressData" :key="index" class="mt-4">
        <p>{{ item.label }}</p>
        <div class="w-full bg-gray-200 rounded-full h-2.5">
          <div class="bg-blue-600 h-2.5 rounded-full" :style="{ width: item.value + '%' }"></div>
        </div>
        <p class="text-right">{{ item.value }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      progressData: Array
    }
  };
  </script>
  
  <style scoped>
  /* Additional styling, if needed */
  </style>
  