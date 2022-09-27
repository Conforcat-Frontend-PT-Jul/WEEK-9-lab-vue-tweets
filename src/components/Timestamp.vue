<template>
  <span className="timestamp">{{ time }}</span>
</template>

<script setup>
defineProps({
  time: {
    type: String,
  },
});
</script>
