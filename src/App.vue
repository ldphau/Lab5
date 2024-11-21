<script setup>
import Bai1 from './components/Bai1.vue'
import Bai2 from './components/Bai2.vue'
import Bai3 from './components/Bai3.vue'
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';
 
import {ref} from 'vue'

const posts = ref([])

function addPost(post){
    posts.value.push(post)
}
</script>
<template>
 
    <!-- <Bai1></Bai1>
    <Bai2></Bai2> 
    <Bai3></Bai3> -->
    <div id="app"> 
        <CreatePost @add-post="addPost"/>
        <PostList :posts="posts" />
    </div>
</template>

