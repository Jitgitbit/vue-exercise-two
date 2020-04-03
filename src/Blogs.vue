<template>
  <div class="blogs">
    <h2>{{blogTitle}}</h2>
    <button @click='changeTitle'>Change Title</button>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name:'Blogs',
  data(){
    return{
      blogTitle:'Blogs',
      posts:[]
    }
  },
  methods:{
    changeTitle(){
      this.blogTitle = 'Amazing Blog Site'
    }
  },
  beforeCreate(){
    alert('beforeCreated Hook')
  },
  created(){
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(response => {
        console.log(response)
        this.posts = response.data
      })
    alert('created Hook')
  },
  beforeUpdate(){
    alert('beforeUpdate Hook')
  }
}
</script>