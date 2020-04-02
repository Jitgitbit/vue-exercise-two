<template>
  <div id="app">
    <h1>{{title}}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
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
