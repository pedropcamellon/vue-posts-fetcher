<script setup>
import Post from './Post.vue';

defineProps({
  posts: Array,
})
</script>

<template>
  <Post class="post" v-for="p in posts" :title="p.title" :body="p.body" />
</template>

<style scoped>
.post {
  margin-block: 2rem;
  border-bottom: solid;
}
</style>
