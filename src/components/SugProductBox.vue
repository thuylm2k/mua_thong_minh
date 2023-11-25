<template>
  <div
    class="group/sug_product w-[224px] h-[390px] flex flex-col flex-nowrap justify-between border border-gray-200 shadow p-2 hover:border-[#FF7227] transition-all"
  >
    <div class="flex flex-col flex-nowrap justify-start">
      <img
        src="https://cf.shopee.vn/file/daab7ed13eadad643d398a5e0f186aa8_tn"
        alt=""
        class="w-[224px] h-[224px]"
      />
      <div class=" mt-2">
        <p class="break-words text-start">
          Hub chia USB7 cổng có công tắc giá rẻ.
        </p>
        <p class="mt-2 text-start font-medium text-[#ef4444]">579.000 ₫</p>
      </div>
    </div>

    <button
      class="w-full py-3 px-4 flex flex-row flex-nowrap items-center justify-center gap-4 text-white rounded-sm bg-[#FF7227]"
    >
      <p>Đến nơi bán</p>
      <i class="bi bi-arrow-right"></i>
    </button>
  </div>
</template>

<script setup>
import { ref, defineProps } from "vue";

defineProps({
  isRate: Boolean,
});

const rate = ref(5);
</script>

<style lang="scss" scoped></style>
