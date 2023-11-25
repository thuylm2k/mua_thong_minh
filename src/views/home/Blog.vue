<template>
  <div class="grid grid-cols-3 gap-4">
    <Post v-for="(item, index) in 3" :key="index" />
  </div>
</template>

<script setup>
import Post from "../../components/Post.vue";
</script>

<style lang="scss" scoped></style>
