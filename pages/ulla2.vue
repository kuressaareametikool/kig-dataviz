<script setup>
const data = [1,0,1,2,2,3,3];
</script>

<template>
<div>
  <pre v-for="d in data" :style="{ opacity: 0.1 + d / 3 }"> {{ d }}</pre>
    </div>
</template>
