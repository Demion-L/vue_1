<template>
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
</template>

<script></script>

<style scoped></style>
