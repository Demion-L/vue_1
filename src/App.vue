<template>
  <div class="app">
    <form @submit.prevent>
      <h4>Create post</h4>
      <input
        v-bind:value="title"
        @input="inputTitle"
        class="input"
        type="text"
        placeholder="Title"
      />
      <input
        v-bind:value="body"
        @input="body = $event.target.value"
        class="input"
        type="text"
        placeholder="Description"
      />
      <button class="btn" @click="createPost">Create</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: "JS", body: "Description of JS" },
        { id: 2, title: "Java", body: "Description of Java" },
        { id: 3, title: "Python", body: "Description of Python" },
      ],
      title: "",
      body: "",
    };
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body,
      };
      this.posts.push(newPost);
      this.title = "";
      this.body = "";
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

form {
  display: flex;
  flex-direction: column;
}
.btn {
  align-self: flex-end;
  margin-bottom: 1px;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-bottom: 15px;
}
</style>
