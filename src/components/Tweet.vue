<script setup>
  import ProfileImage from './ProfileImage.vue';
  import User from './User.vue';
  import Timestamp from './Timestamp.vue';
  import Message from './Message.vue';
  import Actions from './Actions.vue';


  const props = defineProps({
    user: { type: Object, },
    timestamp: { type: String, },
    message: { type: String, },
});
  /*Puedo utilizar el props solo de tweet= Object? pero claro en cada parte debajo en el HTML debo colocar tweet.user.image? y tweet.user, tweet.timestamp?  */
</script>

<template>
  <div className="tweet">
    <ProfileImage v-bind:image="user.image"/>
    <!--<img
      src="https://i.imgur.com/9yw1Fyw.jpg"
      className="profile"
      alt="profile"
    />-->

    <div className="body">
      <div className="top">
        <User v-bind:userData="user" />
        <!--<span className="user">
          <span className="name">Ironhack</span>
          <span className="handle">@ironhack</span>
        </span>-->

        <Timestamp v-bind:time="timestamp"/>
       <!-- <span className="timestamp">Nov 30, 2020</span>-->
      </div>

      <Message v-bind:message="message"/>
      <!--<p className="message">
        On December 7th, we will be hosting a #webinar that will introduce you
        to #SQL! Are you ready? 🚀
      </p>-->

      <Actions />
      <!-- <div className="actions">
         Font Awesome icons 
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>-->
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
