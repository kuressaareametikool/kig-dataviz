<script setup>
//    0 1 2 3 4 5 6
//     E T K N R L P
const data = [5, 6, 5, 7, 9, 6, 5];
</script>

<template>
  <div>
    <pre v-for="d in data" :style="{ opacity: 0.1 + d / 3 }">{{ d }}</pre>
    <svg width="500" height="500" class="bg-gray-100">
      <rect x="50" y="50" width="50" height="50" opacity="0.5" />
      <rect x="100" y="50" width="50" height="50" opacity="0.2" />
      <rect x="150" y="50" width="50" height="50" opacity="0.1" />
      <rect x="200" y="50" width="50" height="50" opacity="0.05" />
    </svg>
  </div>
</template>
