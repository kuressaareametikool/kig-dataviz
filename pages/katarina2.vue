<script setup>
//  i         0  1  2  3  4  5  6   
//            E  T  K  N  R  L  P
const data = [7, 6, 5, 6, 8, 5, 5];
</script>

<template>
  <div>
  <pre v-for="(d, i) in data" :style="{ opacity:0.1 + d / 3 }">{{ d }}</pre>
  <svg width="1000" height="1000" class="bg-gray-100">
   <circle
   v-for="(d, i) in data"
   :style="{ opacity: 0.1 + d / 15, fill: 'dark-gray' }"
        :cx="i * 50 + 50"
        cy="50"
        :r="d * 5"
        width="10"
        height="10"
   />
  </svg>
  </div>
</template>
