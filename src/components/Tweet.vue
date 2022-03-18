<template>
  <div className="tweet">
   
    <ProfileImage :image="tweet.user.image" />

     <div className="body">
      <div className="top">
         <User :name="tweet.user.name" :handle="tweet.user.handle" />

       
         <Timestamp :timestamp="tweet.timestamp" />
      </div>
         <Message :message="tweet.message" /> 
         <Actions /> 
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Message from './Message.vue';
import Timestamp from './Timestamp.vue';
import Actions from './Actions.vue'

export default {
    name:"Tweet",
     props:{
       tweet: Object,
     },
    components: {
      ProfileImage,
      User,
      Message,
      Timestamp,
      Actions,
    },
    mounted(){
      console.log(this.tweet)
    }
    
    }
</script>


<style scoped>
a {
  color: #42b983;
}
</style>
