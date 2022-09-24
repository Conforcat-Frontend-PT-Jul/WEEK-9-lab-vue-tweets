<script setup>
defineProps({
  image: {
    type: String,
  },
});
</script>
<template>
  <img class="profile" :src="image" alt="profile" />
</template>