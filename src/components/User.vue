<template>
  <div class="wrapper">
    <span>{{userInfo.name}}</span>
    <span>{{userInfo.handle}}</span>
  </div>
</template>

<script>
export default {
    props: {
        userInfo: Object
    }
}
</script>

<style>

</style>