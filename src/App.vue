<template>
  <div class="app">
    <PostForm />
    <PostList v-bind:posts="posts" @create="createPost" />
  </div>
</template>

<script>
//import our components
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
    inputTitle(event) {
      this.title = event.target.value;
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
</style>
