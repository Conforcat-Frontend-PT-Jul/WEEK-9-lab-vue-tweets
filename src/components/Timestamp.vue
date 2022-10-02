<script setup>
const props = defineProps({
  timestamp: String,
});
</script>

<template>
  <span className="timestamp"> {{ timestamp }}</span>
</template>
