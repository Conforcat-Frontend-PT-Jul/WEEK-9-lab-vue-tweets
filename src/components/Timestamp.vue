<template>
    <span className="timestamp">{{ time }}</span>
</template>

<script setup>
    const props = defineProps({
        time: String
    });
</script>