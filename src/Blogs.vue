<template>
  <div class="blogs">
    <h2>{{blogTitle}}</h2>
    <button @click='changeTitle'>Change Title</button>
    <input type="text" v-model='searchTerm'>
    <div v-for='post in posts' :key='post.id'>
      <h3>{{post.title}}</h3>
      <p>{{post.body | snippet}}</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name:'Blogs',
  data(){
    return{
      blogTitle:'Blogs',
      posts:[],
      searchTerm:''
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
      .catch(err => {
        console.log(err)
      })
    alert('created Hook')
  },
  beforeUpdate(){
    alert('beforeUpdate Hook')
  }
}
</script>