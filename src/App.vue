<template>
  <div id="app">
    <h1>{{title}}</h1>
    <NavBar/>
  </div>
</template>

<script>
import NavBar from './NavBar'
export default {
  name: 'app',
  components:{
    NavBar: NavBar
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
