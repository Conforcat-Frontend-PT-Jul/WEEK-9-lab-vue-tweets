<template>
  <div className="tweet">
    <profileImage :image="user.image" />

    <div className="body">
      <div className="top">        
          <User :userInfo="user"/>
          <TimeStamp :timeStamp="timestamp" />       
      </div>

      <Message :message="message"/>
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>

  import ProfileImage from './ProfileImage.vue';
  import Actions from './Actions.vue';
  import Message from './Message.vue';
  import TimeStamp from './TimeStamp.vue';
  import User from './User.vue';

  export default{

    props: {
      user: Object,
      timestamp: String,
      message: String
    },

    components:{
      ProfileImage,
      Actions,
      Message,
      TimeStamp,
      User
    },
  }
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
