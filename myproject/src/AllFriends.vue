<template>
  <div id="all-friends">
   <h2>All Friends</h2> 
   <div v-for="(person, index) in friends" :key="index">
<span @click="unfriend(person.name)">{{person.name}}</span>
   </div>
   <div>
</div>
  </div>
</template>
<script>
export default {
  name:'AllFriends',
  props:['friends'],
  data() {
    return {
          
    }
  },
  methods:{
    unfriend(name){
      this.$emit('delete',{name:name})
    }
  }
}
</script>
<style>

</style>
