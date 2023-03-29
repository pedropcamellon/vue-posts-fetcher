<script setup>
defineProps({
  title: String,
  body: String,
})
</script>

<template>
  <div>
    <h4 class="title">{{ title }}</h4>
    <p class="body">{{ body }}</p>
  </div>
</template>

<style scoped>
</style>
