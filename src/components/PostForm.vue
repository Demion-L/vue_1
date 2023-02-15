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
    <button class="btn">Create</button>
  </form>
</template>

<script></script>

<style scoped>
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
