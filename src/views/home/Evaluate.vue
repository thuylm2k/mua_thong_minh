<template>
  <div>
    <p class="mb-5 text-lg font-medium">Đánh giá từ người mua</p>
    <div v-for="(item, index) in 5" :key="index">
      <Assess />
      <el-divider />
    </div>
    <div class="flex justify-center">
      <button class="p-3 border border-slate-950 rounded">Xem thêm</button>
    </div>
  </div>
</template>

<script setup>
import Assess from "../../components/​Assess.vue";
</script>

<style lang="scss" scoped></style>
