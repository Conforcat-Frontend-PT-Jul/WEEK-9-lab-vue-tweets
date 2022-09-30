<script setup>
    const props = defineProps({
      message: {
        type: String,
      },
    });
</script>

<template>
    <p className="message"> {{ message }} </p>
</template>