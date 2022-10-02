<script>
    export default{
        props:{
            image: String,
        },
    }
</script>

<template>
    <img :src="image" alt="profile" className="profile">
</template>