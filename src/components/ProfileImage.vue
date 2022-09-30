<script setup>
    const props = defineProps({
      image: {
        type: String,
      },
    });
</script>

<template>
      <img
      v-bind:src="image" 
      class="profile" 
      alt="profile" />
</template>

<style scoped>
    
</style>