<template>
   <div class="home">
     <h1> {{post.title}} </h1>
     <p> {{post.body}} </p>
   </div>
</template>
<script>
import axios from 'axios'
export default {
  data(){
    return{
      post: {}
    }
  },
  created(){
    axios.get('https://jsonplaceholder.typicode.com/posts/'+this.$route.params.id).then(res=>{
      this.post = res.data
    })
  },
  head() {
      return {
        title: this.post.title+' - Tech Blog',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: this.post.body
          }
        ]
      }
    }
}
</script>
<style >
.home{
  margin: 10px;
}
</style>
