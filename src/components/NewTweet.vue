<template>
    <div className="tweet">
      <ProfileImage :image="user.image"/>
  
      <div className="body">
        <div className="top">
          <CompUser :user="user"/>
          <TimesTap :timestamp="timestamp"/>
        </div>
        <NewMessage :message= "message" />
      <NewActions />
    </div> 
       <i class="fas fa-ellipsis-h"></i>
    </div>
  </template>
  <script>
  import ProfileImage from "./ProfileImage.vue";
  import CompUser from './CompUser.vue';
  import TimesTap from "./TimesTap.vue";
  import NewMessage from "./NewMessage.vue";
  import NewActions from "./NewActions.vue";
    export default {
    props: {
        user: {
            name: String,
            image: String,
            handle: String,
        },
        timestamp: String,
        message: String,
    },
    components: {
    ProfileImage,
    CompUser,
    TimesTap,
    NewMessage,
    NewActions,
},
}
  </script>
  <style scoped>
  a {
    color: #42b983;
  }
  </style>