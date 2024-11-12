<template>
    <div class="card bg-white shadow p-4 rounded-lg mb-4">
      <h2 class="text-gray-700 font-semibold">{{ title }}</h2>
      <ul>
        <li v-for="item in summaryData" :key="item.id" class="flex items-center mt-2">
          <span class="icon text-lg">{{ item.icon }}</span>
          <p class="ml-2">{{ item.text }}</p>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      summaryData: Array
    }
  };
  </script>
  