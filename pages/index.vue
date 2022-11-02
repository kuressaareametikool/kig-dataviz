<script setup>
const { data } = await useSheet(
  "1rq0SknbfsfC3fcxt_vMMX_-KQX8hNmAGF98OB7r3PSU",
  "värvidkokku"
);
</script>

<template>
  <div v-for="col in range(1, 8)" class="pt-12">
    {{ data[0][col] }}
    <p
      v-for="row in range(1, 12)"
      :style="{
        width: data[row][col] * 50 + 'px',
        background: data[row][0],
        color: 'darkgray',
        padding: '5px 10px',
      }"
    >
      {{ data[row][0].slice(0, 10) }}
    </p>
  </div>
</template>
