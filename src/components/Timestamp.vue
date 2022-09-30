<script setup>
    const props = defineProps({
      time: {
        type: String,
      },
    });
</script>

<template>
    <span className="timestamp"> {{ time }} </span>
</template>