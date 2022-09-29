<template>
  <div className="tweet">
    <img
      :src= tweet[0].user.image
      className="profile"
      alt="profile"
    />

    <div className="body">
      <div className="top">
        <span className="user">
          <span className="name">{{tweet[0].user.name}}</span>
          <span className="handle">@{{tweet[0].user.handle}}</span>
        </span>

        <span className="timestamp">{{tweet[0].timestamp}}</span>
      </div>

      <p className="message">
       {{tweet[0].message}}
      </p>

      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
  export default{

    props: {
      tweet: Array
    },

    setup(props){

      console.log(props.tweet);

      return{

      }
    }
  }
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
