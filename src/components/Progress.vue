<template>
  <div class="inline-block text-sm bg-gray-200 rounded-full overflow-hidden relative"
    style="background-color: #333336;">
    <div class="px-2 text-sm transition-[width] duration-500 whitespace-nowrap" :class="{
      'bg-stone-900': value / max < 0.8,
      'bg-blue-900/90': value / max >= 0.8 && value / max < 0.9,
      'bg-rose-950': value / max >= 0.9,
    }" :style="{
        width: `${value / max * 100}%`,
      }">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  value: number
  max: number
}>()
</script>
