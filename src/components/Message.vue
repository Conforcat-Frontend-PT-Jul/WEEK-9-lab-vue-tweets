<template>
    <span className="message">{{msg}}</span>
</template>
  
<script>

export default {
    name: 'Message',
    props: {
        msg: String
    },
    data() {

    },
}
</script>