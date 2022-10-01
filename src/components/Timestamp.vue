<script setup>
defineProps({
  timestamp: String,
});
</script>

<template>
  <span className="timestamp">{{ timestamp }}</span>
</template>
