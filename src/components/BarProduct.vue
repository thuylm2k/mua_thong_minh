<script setup>
import { ref } from "vue";

const rate = ref(5);
</script>

<template>
  <div class="p-5 flex flex-row flex-nowrap justify-between shadow-xl rounded-lg">
    <div class="flex flex-row flex-nowrap items-center gap-3">
      <img
        src="https://cf.shopee.vn/file/3ec4bce7a0fa680286ec55f4ac16ea71_tn"
        alt="image"
        class="w-[80px] h-[80px]"
      />
      <div>
        <p class="text-basa font-medium">
          Bộ chia cổng type-c baseus metal gleam series cahub-cw0g
        </p>

        <div class="flex flex-row flex-nowrap items-center gap-2 text-xs">
          <div class="flex flex-row flex-nowrap items-center gap-2">
            <p class="text-[#F7BA2A]">{{ rate }}</p>
            <el-rate v-model="rate" allow-half disabled />
          </div>

          <p>59 đánh giá</p>

          <p class="pl-3 border-l-2 border-[#d1d5db]">199 lượt bán</p>
        </div>
      </div>
    </div>

    <div class="flex flex-row flex-nowrap items-center gap-3">
      <p class="text-base font-medium text-[#dc2626]">650.000 ₫</p>
      <button
        class="py-3 px-4 flex flex-row flex-nowrap items-center gap-4 text-[#1b5af2] border border-[#1b5af2] rounded-[4px]"
      >
        <span>Đến nơi bán</span>
        <i class="bi bi-arrow-right"></i>
      </button>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
