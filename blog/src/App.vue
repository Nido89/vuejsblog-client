<template>
  <div id="app">
 <Header />
 <Latest :posts="posts"  />
 <Posts :posts="posts" :count="postCount" @showMore="this.showMore"/>


  </div>
</template>

<script>
import Header from './components/Header';
import Latest from './components/Latest';
import Posts from './components/Posts';
export default {
  name: 'App',
  data () {
    return{
      API_URL:"http://localhost:3000/api/",
      posts:[],
      postCount:6
    }
  },
  components: {Header,Latest,Posts},
  methods: {
    getPosts() {
      fetch(this.API_URL+"posts/all")
      .then(data => {
        return data.json();

      })
      .then(json => {
        this.posts = json.result;
        this.posts = this.posts.sort(function (a,b){
          if(a.timestamp <b.timestamp){
            return 1;
          }
          if(a.timestamp > b.timestamp) {
            return -1;
          }
          return 0;
        });
        
      });
    },
    showMore () {
      this.postCount += 2;
    }
  },
  beforeMount(){
    this.getPosts();
  }
}
</script>

<style lang="scss">
body{
  background-color:lightgoldenrodyellow ;
  font-family: 'Times New Roman', Times, serif, Haettenschweiler, 'Arial Narrow Bold';

  h3{
    color: teal;
    font-size: 28px;
    font-weight: 700;
  }
}
</style>
