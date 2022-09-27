<template>
  <div className="tweet">
    <ProfileImage :image="tweet.user.image"></ProfileImage>

    <div className="body">
      <div className="top">
        <User :user="tweet.user"></User>

        <Timestamp :timestamp="tweet.timestamp"></Timestamp>
      </div>

      <Message :msg="tweet.message"></Message>

      <TheActions></TheActions>
    </div>

    <i class="fas fa-ellipsis-h" :src="tweet.user.image"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import TheActions from './TheActions.vue';

export default {
    name: "Tweet",
    props: {
        tweet: Object
    },
    data() {
    },
    methods: {},
    computed: {},
    components: { ProfileImage, User, Timestamp, Message, TheActions }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
