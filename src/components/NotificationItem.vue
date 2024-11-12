<template>
    <div class="card bg-white shadow p-4 rounded-lg mb-4">
      <h2 class="text-gray-700 font-semibold">ឯកសាទទួលបាន</h2>
      <ul>
        <li v-for="(notification, index) in notifications" :key="index" class=" mt-2">
        <p>{{ notification.icon }}</p> <p>  {{ notification.text }}</p>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        notifications: [
          { icon: '💰' },
          { text: 'New document uploaded' },
          { text: 'Reminder to check files' }
        ]
      };
    }
  };
  </script>
  