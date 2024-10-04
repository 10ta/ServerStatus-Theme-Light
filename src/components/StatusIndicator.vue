<template>
  <div
    class="rounded-full inline-block"
    :class="{
      'bg-green-900': status,
      'bg-red-900': !status,
    }"
  />
</template>

<script setup lang="ts">
defineProps<{
  status: boolean
}>()
</script>
