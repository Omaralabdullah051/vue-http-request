<template>
    <div>
       <!-- <button @click="getPosts">Load Posts</button> -->
       <h3 v-if="errorMsg">{{errorMsg}}</h3>
       <div v-for="post in posts" :key="post.id">
        <h3>{{post.id}} {{post.title}}</h3>
        <p>{{post.body}}</p>
        <hr>
       </div>
    </div>
</template>

<script>
import axios from "axios";
    export default {
        name: 'PostList',
        created(){
            this.getPosts();
        },
        data(){
            return{
                posts: [],
                errorMsg: ''
            }
        },
        methods:{
            getPosts(){
              axios.get('https://jsonplaceholder.typicode.com/posts')
              .then((data) => {
                console.log(data.data);
                this.posts = data.data;
              })
              .catch(err => {
                console.log(err);
                this.errorMsg = 'Error retrieving data'
              })
            }
        }
    }
</script>

<style scoped>

</style>