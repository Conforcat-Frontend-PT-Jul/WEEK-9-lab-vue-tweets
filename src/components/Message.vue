<script setup>
defineProps({
  message: String,
});
</script>

<template>
  <p className="message">{{ message }}</p>
</template>
