<template>
  <div id="app">
    <h1>{{title}}</h1>
    <NavBar/>
    <AllFriends/>
    <OnlineFriends/>
  </div>
</template>

<script>
import NavBar from './NavBar'
import AllFriends from './AllFriends'
import OnlineFriends from './OnlineFriends'

export default {
  name: 'app',
  components:{                        // ES6 refactoring:         NavBar: NavBar   ==     NavBar    !!!
    NavBar,
    AllFriends,
    OnlineFriends                                 
  },
  data () {
    return {
      title:'A new Vue App, wohoo ;)'
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
