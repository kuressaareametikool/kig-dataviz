<script setup>
import { random } from "~~/composables/math";

const { data } = await useSheet(
  "1rq0SknbfsfC3fcxt_vMMX_-KQX8hNmAGF98OB7r3PSU",
  "iris"
);

const nudge = 3;
</script>

<template>
  <div>
    <svg width="500" height="750" xmlns="http://www.w3.org/2000/svg">
      <rect width="500" height="750" fill="#eee" />
      <g v-for="(cols, row) in data">
        <g v-for="(value, col) in cols">
          <circle
            :style="{
              opacity: 1,
              stroke: cols[7],
              fill: 'none',
              strokeWidth: 3,
            }"
            :cx="col * 50 + 100 + random(-nudge, nudge)"
            :cy="0 * 3 + 100 + random(-nudge, nudge)"
            :r="area2radius(parseInt(value)) * 15"
          />
        </g>
      </g>

      <g transform="translate(0,200)">
        <g v-for="(cols, row) in data">
          <g v-for="(value, col) in cols">
            <circle
              :style="{
                opacity: 1,
                stroke: cols[7],
                fill: 'none',
                strokeWidth: 3,
              }"
              :cx="col * 50 + 100 + random(-nudge, nudge)"
              :cy="0 * 3 + 100 + random(-nudge, nudge)"
              :r="area2radius(parseInt(value)) * 15"
            />
          </g>
        </g>
      </g>

      <text x="200" y="680" opacity="0.4" fontFamily="sans-serif">
        E T K N R L P
      </text>
    </svg>
  </div>
</template>
