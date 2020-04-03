<template>
  <div id="app">
    <h1>{{title}}</h1>
    <NavBar/>
    <AllFriends :friends="friends" @delete='deleteFriend' />
    <OnlineFriends :friends='friends'/>
    <Blogs/>
  </div>
</template>

<script>
import NavBar from './NavBar'
import AllFriends from './AllFriends'
import OnlineFriends from './OnlineFriends'
import Blogs from './Blogs'

export default {
  name: 'app',
  components:{                        // ES6 refactoring:         NavBar: NavBar   ==     NavBar    !!!
    NavBar,
    AllFriends,
    OnlineFriends,
    Blogs                                 
  },
  data () {
    return {
      title:'A new Vue App, wohoo ;)',
      friends:[
        {name:'Luigi', online: true},
        {name:'Mario', online: false},
        {name:'Peter', online: true},
        {name:'Mark', online: false},
      ]
    }
  },
  methods: {
    deleteFriend(payload){
      console.log(payload)
      this.friends = this.friends.filter(friend => {
        return friend.name !== payload.name
      })
    }
  }
}
</script>

<style>
h1{
  font-weight: normal;
  text-align: center;
  color: #2c3e50;
}
</style>
