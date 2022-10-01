<template>
    <span className="timestamp">{{ timeStamp }}</span>
</template>

<script setup>
    const props = defineProps({
        timeStamp: String,
    })
</script>