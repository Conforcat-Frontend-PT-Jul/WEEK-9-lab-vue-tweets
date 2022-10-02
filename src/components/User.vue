<script setup>
const props = defineProps({
  name: String,
  handle: String,
});
</script>

<template>
  <span className="user">
    <span className="name"> {{ name }} </span>
    <span className="handle">@{{ handle }}</span>
  </span>
</template>
