<script setup>
defineProps({
  image: String,
  name: String,
});
</script>

<template>
  <img :src="image" className="profile" alt="profile" />
</template>
