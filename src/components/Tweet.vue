<script setup>
import { objectToString } from "@vue/shared";
import { stringify } from "postcss";
import { computed } from "vue";
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

const props = defineProps({
  tweet: Object,
});

const tweetData = computed(() => props.tweet.user);
</script>

<template>
  <div className="tweet">
    <ProfileImage :image="tweetData.image" />

    <div className="body">
      <div className="top">
        <User :name="tweetData.name" :handle="tweetData.handle" />
        <Timestamp :timestamp="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />
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
