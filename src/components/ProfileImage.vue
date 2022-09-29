<script>
export default {
    props: {
        image: String,
    },
};
</script>

<template>
    <img :src="image" className="profile" alt="profile" />
</template>

<style scoped>

</style>