<script setup>
const { data } = await useSheet(
  "1dh-71mDVPeiB7mvQn-EUal-4p1swJHE3d5FqwoPVwTQ",
  "Sheet1"
);
</script>

<template>
  <div>
    <pre>{{ data }}</pre>
  </div>
</template>
