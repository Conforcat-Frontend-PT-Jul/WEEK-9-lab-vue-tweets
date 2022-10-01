<template>
<img :="image" className="profile"/>
</template>

<script>
export default {
  data(){
    return{
      image:{
        src:"https://i.imgur.com/b0EdHVV.jpg",
        alt:"profile"
      }
    }
  }

};
</script>