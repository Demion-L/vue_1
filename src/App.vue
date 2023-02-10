<template>
  <div>
    <button>Like</button>
    <button></button>
  </div>
  <div>
    Likes: <strong>{{ likes }}</strong>
  </div>
  <div>
    Dislikes: <strong>{{ dislikes }}</strong>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 5,
    };
  },
  methods: {
    addLike() {
      this.likes += 1;
    },
    addDislike() {
      this.likes += 1;
    },
  },
};
</script>

<style></style>
