<template>
  <div class="container">
    <div class="i" v-for="item in posts" :key="item.id">
      <v-col  cols="12">
          <v-card
            color="#385F73"
            dark
          > <div class="t">
            <nuxt-link class="link" :to="`/details/${item.id}`"> <v-card-title class="headline">
              {{item.title}}
            </v-card-title>
            </nuxt-link>

            <v-card-subtitle> {{item.body}} </v-card-subtitle>
           </div>
          </v-card>
        </v-col>
    </div>
      <h1>{{e}}</h1>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data(){
    return{
      posts: [],
      e: ""
    }
  },
  created(){
    axios.get('https://jsonplaceholder.typicode.com/posts')
    .then(res=>{
        this.posts =  res.data
    }).catch(e=>{
      this.e += e
    })
  }
}
</script>

<style>
.link{
  text-decoration: none;
  color: white;
}
.container {
  margin: 3px;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.i{
  margin: 5px;
  text-align: center;
}

</style>
