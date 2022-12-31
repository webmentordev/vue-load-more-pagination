<template>
  <div class="max-w-4xl m-auto px-4 py-6 grid grid-cols-3 gap-6">
    <div v-for="post in posts" :key="post.id" class="bg-gray-900 p-6 rounded-lg text-white">
      <p>{{ post.body }}</p>
    </div>
  </div>
  <div class="flex justify-center w-full">
    <button v-show="final" @click="loadMore" class="bg-blue-600 text-white m-auto py-2 px-4 rounded-md">Load More</button>
    <span v-if="final == false" @click="loadMore" class="text-gray-700 py-6">No more data exist in database</span>
  </div>
</template>

<script>


export default {
  name: 'HomeView',
  data(){
    return{
      posts: [],
      page: 1,
      postLimit: 3,
      final: true
    }
  },
  mounted() {
    fetch(`http://localhost:3000/posts?_page=${this.page}&_limit=${this.postLimit}`)
    .then((res) => res.json())
    .then(data => {
      this.posts = data
      console.log(this.page, this.posts);
    }).catch(error => {
        console.log(error)
      })
    
  },
  methods: {
    loadMore(){
      this.page++;
      fetch(`http://localhost:3000/posts?_page=${this.page}&_limit=${this.postLimit}`)
      .then((res) => res.json())
      .then(data => {
        this.posts.push(...data)
        if(data.length < this.postLimit){
          this.final = false
        }
      })
      .catch(error => {
        console.log(error)
      })
    }
  }
}
</script>
