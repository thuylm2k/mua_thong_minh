<script setup>
</script>

<template>
  <div>
    <p class="text-lg font-semibold">Lịch sử giá</p>

    <div class="p-4 mt-4 border border-[#cd7740] rounded">
      <div class="flex flex-row flex-nowrap items-center justify-between gap-2">
        <p
          class="text-lg font-semibold text-[#cd7740] flex flex-row flex-nowrap items-center"
        >
          <span> Biến động giá </span>
          <img
            src="images/lg_mua_thong_minh.png"
            alt="logo"
            class="w-[24px] h-[24px]"
          />
        </p>
        <p>Giá hiện tại: <strong class="text-lg">669.000 ₫</strong></p>
      </div>

      <div
        class="mt-3 flex flex-row flex-nowrap items-center justify-end gap-4"
      >
        <span>Từ</span>
        <span class="px-2 py-1 bg-[#E5E7EB]">01-03-2023</span>

        <span>Đến</span>
        <span class="px-2 py-1 bg-[#E5E7EB]">01-03-2023</span>
      </div>

      <div
        class="mt-2 flex flex-row flex-nowrap items-center justify-start gap-5 text-sm"
      >
        <span>
          <span>Cao nhất:</span>
          <span class="text-[#f87171]">888.000 ₫</span>
        </span>

        <span>
          <span>Thấp nhất:</span>
          <span class="text-[#059669]">333.000 ₫</span>
        </span>
      </div>

      <div class="mt-3">
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
