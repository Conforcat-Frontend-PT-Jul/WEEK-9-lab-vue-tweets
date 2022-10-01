<template>
  <div className="tweet">
    <ProfileImage  />

    <div className="body">
      <div className="top">
        <User :userData="tweet.user" />
        <TimeStamp :timestamp="tweet.timestamp"/>
      </div>
      <Message :message="tweet.message" />
      <Actions />
     
  
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>
  import ProfileImage from "./ProfileImage.vue";
  import Actions from "./Actions.vue";
  import Message from "./Message.vue";
  import User from "./User.vue";
  import TimeStamp from "./TimeStamp.vue";

  export default{
    
    props: {
    tweet: Object,
  
  },
  components: { ProfileImage, Actions, Message, User,TimeStamp  }
  }
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
