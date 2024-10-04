<template>
  <div
    class="rounded-full inline-block"
    :class="{
      'bg-green-600': status,
      'bg-red-800': !status,
    }"
  />
</template>

<script setup lang="ts">
defineProps<{
  status: boolean
}>()
</script>
