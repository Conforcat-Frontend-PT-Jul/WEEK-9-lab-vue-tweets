<template>
  <div class="wrapper">
    <img
      :src= "image"
      className="profile"
      alt="profile"
    />
  </div>
</template>

<script>
export default {
    props: {
        image: String
    }
}
</script>

<style>

</style>