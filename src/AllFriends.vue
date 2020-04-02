<template>
  <div id="all-friends">
    <h2>All Friends</h2>
    <div v-for='friend in friends'>
      <span>{{friend.name}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name:'AllFriends',
  data(){
    return{
      friends:[
        {name:'Luigi', online: true},
        {name:'Mario', online: false},
        {name:'Peter', online: true},
        {name:'Mark', online: false},
      ]
    }
  }
}
</script>

<style>

</style>