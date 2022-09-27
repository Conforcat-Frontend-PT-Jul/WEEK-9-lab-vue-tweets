<script setup>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

const props = defineProps({
  tweet: Object,
});
</script>

<template>
  <div className="tweet">
    <ProfileImage :image="tweet[0].user.image" :name="tweet[0].user.name" />

    <div className="body">
      <div className="top">
        <User :name="tweet[0].user.name" :handle="tweet[0].user.handle" />
        <Timestamp :timestamp="tweet[0].timestamp" />
      </div>

      <Message :message="tweet[0].message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>

<!-- <img :src="tweet[0].user.image" className="profile" alt="profile" /> -->

<!-- <span className="user">
  <span className="name">{{ tweet[0].user.name }}</span>
  <span className="handle">{{ tweet[0].user.handle }}</span>
</span> -->

<!-- <span className="timestamp">{{ tweet[0].timestamp }}</span> -->

<!-- <p className="message">
  {{ tweet[0].message }}
</p> -->

<!-- <div className="actions">
  <i class="far fa-comment"></i>
  <i class="fas fa-retweet"></i>
  <i class="far fa-heart"></i>
  <i class="fas fa-share"></i>
</div> -->
