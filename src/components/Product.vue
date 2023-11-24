<script setup>
import { ref } from "vue";

const imgsSlider = [
  {
    img: "https://cf.shopee.vn/file/38625d8696c075b0266676b87dc910dd_tn",
    imgView: "https://cf.shopee.vn/file/38625d8696c075b0266676b87dc910dd",
  },
  {
    img: "https://cf.shopee.vn/file/0831df249013d5ae50d7ed42996412c8_tn",
    imgView: "https://cf.shopee.vn/file/0831df249013d5ae50d7ed42996412c8",
  },
  {
    img: "https://cf.shopee.vn/file/b8bbded9005be18fae9ce3819b29ef8d_tn",
    imgView: "https://cf.shopee.vn/file/b8bbded9005be18fae9ce3819b29ef8d",
  },

  {
    img: "https://cf.shopee.vn/file/38625d8696c075b0266676b87dc910dd_tn",
    imgView: "https://cf.shopee.vn/file/38625d8696c075b0266676b87dc910dd",
  },
  {
    img: "https://cf.shopee.vn/file/0831df249013d5ae50d7ed42996412c8_tn",
    imgView: "https://cf.shopee.vn/file/0831df249013d5ae50d7ed42996412c8",
  },
  {
    img: "https://cf.shopee.vn/file/b8bbded9005be18fae9ce3819b29ef8d_tn",
    imgView: "https://cf.shopee.vn/file/b8bbded9005be18fae9ce3819b29ef8d",
  },
];

const imgView = ref(
  "https://cf.shopee.vn/file/be82e16ddc37dcf2657d02a30171a050"
);

const rate = ref(4.5);
</script>

<template>
  <div class="w-full flex flex-row flex-nowrap gap-5 mt-5">
    <div class="w-1/2 p-3 border rounded-lg">
      <img :src="imgView" alt="" />
      <div
        class="scroll_list_product max-w-full h-[115px] px-2 mt-3 flex flex-row flex-nowrap gap-2 overflow-x-auto"
      >
        <div
          class="h-fit border border-slate-400"
          v-for="(item, index) in imgsSlider"
          :key="index"
        >
          <img
            :src="item.img"
            alt="image"
            class="min-w-[90px] w-[90px] h-[90px]"
          />
        </div>
      </div>
    </div>
    <div class="w-1/2">
      <p class="text-lg font-semibold">
        Bộ Hub mở rộng Baseus Metal Gleam StarJoy Series 8 in 1 4K60Hz
      </p>

      <div
        class="w-fit mt-3 flex flex-row flex-nowrap items-center justify-center gap-2 px-4 py-1 border border-[#FF7227] rounded-3xl text-[#FF7227]"
      >
        <i class="bi bi-bell text-xl"></i>
        <p class="text-base font-semibold">Theo dõi giảm giá</p>
      </div>

      <div class="w-fit flex flex-row flex-nowrap items-center gap-4 mt-3">
        <p>Giá từ Shopee</p>
        <img
          src="https://lh3.googleusercontent.com/mvI9jsrKjP7Q7ZqYOXuJTRZF9Q1e4PZJjjmNAyzh6OKtxtSUNPK920MMFsXploU60VPMqHCdJLEMzaEF_ktvIXuII2IEamnw0Cr5Cb97_803ePqQQYOLtHQLrVUe9e2DPZ3MoxTp"
          alt=""
          class="rounded-full w-9 h-9"
        />
      </div>

      <div class="flex flex-row flex-nowrap items-center gap-12">
        <div>
          <p class="text-2xl text-[#DC2626] font-bold">669.000 ₫</p>
          <p class="text-md line-through">579.000 ₫</p>
        </div>

        <span
          class="flex flex-row flex-nowrap items-center gap-2 py-2 px-2 text-xs bg-[#FCE7F3] text-[#DC2626] rounded-lg"
        >
          <i class="bi bi-graph-down-arrow"></i>
          <p class="font-semibold">29.790 ₫</p>
        </span>

        <button
          class="py-3 px-4 flex flex-row flex-nowrap items-center gap-4 text-white rounded-md bg-[#FF7227]"
        >
          <p>Đến nơi bán</p>
          <i class="bi bi-arrow-right"></i>
        </button>
      </div>

      <div class="mt-4 flex flex-row flex-nowrap items-center gap-2">
        <div class="flex flex-row flex-nowrap items-center gap-2">
          <p class="text-[#F7BA2A]">{{ rate }}</p>
          <el-rate v-model="rate" allow-half disabled size="large" />
        </div>

        <p class="pl-3 border-l-2 border-[#d1d5db]">59 đánh giá</p>

        <p class="pl-3 border-l-2 border-[#d1d5db]">199 lượt bán</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.scroll_list_product {

}
</style>
