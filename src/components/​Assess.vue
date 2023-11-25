<template>
  <div>
    <div class="flex flex-row flex-nowrap items-start gap-4">
      <div class="flex flex-row flex-nowrap items-center gap-4">
        <el-avatar
          :size="45"
          src="https://cf.shopee.vn/file/3958d01eeaaf632ee0bb594590303a22_tn"
        />
        <span>
          <p class="text-xs">aabbcc1999</p>
          <el-rate v-model="rate" disabled size="small" />
        </span>
      </div>
      <span class="text-[#10b981] text-xs">
        <i class="bi bi-patch-check"></i>
        <span class="pl-1 font-medium">Đã mua tại Shopee</span>
      </span>
    </div>
    <p class="py-2">Sản phẩm tốt</p>
    <div class="flex flex-row flex-nowrap gap-2">
      <span v-for="(item, index) in 5" :key="index">
        <img
          src="https://cf.shopee.vn/file/1fa4aba5bdbd00aae40a1ffa5e6b8bc5_tn"
          alt="image"
          class="w-[80px] h-[80px]"
        />
      </span>
    </div>
    <p class="mt-2 text-xs text-[#6b7280]">1 năm trước</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

const rate = ref(5);
</script>

<style lang="scss" scoped></style>
