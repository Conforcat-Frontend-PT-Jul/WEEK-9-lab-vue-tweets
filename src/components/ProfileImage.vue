<template>
  <img :src="image" alt="profile" class="profile" />
</template>

<script setup>
defineProps({
  image: {
    type: String,
  },
});
</script>
