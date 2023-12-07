<script setup>
defineProps({
  children: Object,
});
</script>

<template>
  <div class="rounded-lg p-10 flex sm:flex-col md:flex-col justify-center items-center gap-6">
    <slot></slot>
  </div>
</template>
