<script setup>
import { ref, onMounted } from 'vue'
import Posts from './components/Posts.vue'

const posts = ref([])

// lifecycle hooks
onMounted(() => {
  fetch('https://jsonplaceholder.typicode.com/posts?_limit=5')
    .then((response) => response.json())
    .then((data) => {
      // Populate 'posts' state variable
      posts.value = data;
    })
    .catch((err) => {
      console.log(err.message);
    });
})
</script>

<template>
  <Posts :posts="posts" />
</template>

<style scoped></style>
