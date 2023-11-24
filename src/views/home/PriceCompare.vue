<script setup>
import BarProduct from "../../components/BarProduct.vue";
</script>

<template>
  <div id="price_compare">
    <p class="mb-8 text-lg font-semibold">So sánh giá</p>

    <p class="mb-4">
      Tìm thấy <strong>13</strong> nơi bán khác, giá từ
      <strong>649.000 ₫ - 719.000 ₫</strong>
    </p>

    <!-- Product -->
    <div class="grid grid-cols-1 gap-4">
      <!-- Shopee -->
      <div>
        <img
          src="https://lh3.googleusercontent.com/OwDr2GswbeYne43OtdOL1cqPx_Q7MoXNPbGAAalXumcCojcbb-KcUQqjP4l2EHOPXySoPWqk5YKDcRqT4_22Yv0L0g0NS6owVBz5ZRFCmUEyyC3NcZd4Nndb6vLEkFJ6k29I5fOb=w556-h50-no"
          alt="logo"
          class="h-10"
        />
        <div class="mt-3 grid grid-cols-1 gap-4">
          <BarProduct v-for="(item, index) in 3" :key="index" />
        </div>
      </div>

      <!-- Lazada -->
      <div>
        <img
          src="https://lh3.googleusercontent.com/DF4aF5VZEz_NYkI_eJIyYFD6SM21UyBxiEeWVRaYY3Cr-MUZ8AuUgB6kI6L6DBCzmCJf7TIMRQYdHgZ9m4WEA4e41oglDoWQIpwoK0Tj784azJsPky9g3w6tUR7mhsfi4U8o_NSGJw=w765-h50-no"
          alt="logo"
          class="h-10"
        />
        <div class="mt-3 grid grid-cols-1 gap-4">
          <BarProduct v-for="(item, index) in 3" :key="index" />
        </div>
      </div>

      <!-- Tiki -->
      <div>
        <img
          src="https://lh3.googleusercontent.com/VaYiFU3XqGRArjLz8nZhSv2VWl39KbeU3Kv3HiK7c5LNA-JqSRZo22Ds2JK0kK04SENns6F8c-vrtQLlC7VHkvh3Y-grYu2HKF6hVAfY0rH_ivBDwdQXB2wc1hkPbBNjp_2Sme5wTA=w515-h50-no"
          alt="logo"
          class="h-10"
        />
        <div class="mt-3 grid grid-cols-1 gap-4">
          <BarProduct v-for="(item, index) in 3" :key="index" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
