<script>
import Actions from "./Actions.vue";
import Message from "./Message.vue";
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";

export default {
  name: 'Tweet',
  props: {
    user: Object,
    message: String,
    timestamp: String,
  },
  components: {
    Actions,
    Message,
    ProfileImage,
    Timestamp,
    User,
  },
};
</script>

<template>
  <div className="tweet">
    <ProfileImage :image="user.image" />
    <div className="body">
      <div className="top">
        <User :userData= "user" />
        <Timestamp :time= "timestamp"/>
      </div>
    <Message :message="message" />
    <Actions/>
    </div>
    <i class="fas fa-ellipsis-h"></i>
  
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
