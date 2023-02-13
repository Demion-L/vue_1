<template>
  <div class="post" v-for="post in posts">
    <div><strong>Name:</strong> {{ post.title }}</div>
    <div><strong>Description:</strong>{{ post.body }}</div>
  </div>
</template>

<script></script>

<style scoped>
.post {
  margin-bottom: 1px;
  padding: 15px;
  border: 2px solid teal;
}
</style>
