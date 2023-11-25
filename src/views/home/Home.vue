<script setup>
import { ref } from "vue";
import Product from "./Product.vue";
import PriceCompare from "./PriceCompare.vue";
import HistoryPrice from "./HistoryPrice.vue";
import ProductDescription from "./ProductDescription.vue";
import Evaluate from "./Evaluate.vue";
import RelatedProduct from "./RelatedProduct.vue";
import Suggest from "./Suggest.vue";
import Blog from "./Blog.vue";
import SuggestionToday from "./SuggestionToday.vue";

const infoTabs = ref(1);

const handleInfoTabs = () => {};
</script>

<template>
  <header
    class="flex flex-row items-center justify-center gap-20 py-6 border-b border-slate-250"
  >
    <p class="text-xl font-bold text-[#F5701A]">Mua Thông Minh</p>

    <div
      class="w-[500px] px-4 py-1.5 flex flex-row flex-nowrap items-center gap-2 border border-black rounded-3xl"
    >
      <input
        type="text"
        class="w-full focus:outline-0"
        placeholder="Dán link hoặc tìm sản phẩm"
      />
      <button>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="currentColor"
          class="bi bi-search"
          viewBox="0 0 16 16"
        >
          <path
            d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
          />
        </svg>
      </button>
    </div>

    <div>
      <ul class="flex flex-row flex-nowrap items-center gap-4 text-lg">
        <li>
          <button class="flex flex-row flex-nowrap items-center gap-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="28"
              height="28"
              fill="currentColor"
              class="bi bi-list"
              viewBox="0 0 16 16"
            >
              <path
                fill-rule="evenodd"
                d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"
              />
            </svg>
            <span>Danh mục</span>
          </button>
        </li>
        <li>
          <button>
            <span>Blog</span>
          </button>
        </li>
      </ul>
    </div>
  </header>

  <main
    class="w-full mt-3 flex flex-col flex-nowrap justify-center items-center bg-white"
  >
    <section class="w-[1024px]">
      <ul class="flex flex-row flex-nowrap items-center gap-3 text-sm">
        <li>
          <img src="/icons/house.svg" alt="" />
        </li>
        <li>
          <img src="/icons/chevron-right.svg" alt="" />
        </li>
        <li class="font-medium">Máy tính & Laptop</li>
        <li>
          <img src="/icons/chevron-right.svg" alt="" />
        </li>
        <li class="font-medium">Phụ Kiện Máy Tính</li>
        <li>
          <img src="/icons/chevron-right.svg" alt="" />
        </li>
        <li class="font-medium">Bộ chia cổng USB & Đọc thẻ nhớ</li>
      </ul>

      <Product />

      <div class="w-3/4 mt-8">
        <el-tabs
          v-model="infoTabs"
          id="product_info_tab"
          class=""
          @tab-click="handleInfoTabs"
        >
          <el-tab-pane label="User" :name="1">
            <template #label>
              <span
                class="flex flex-row flex-nowrap items-center gap-2 text-base"
                :class="infoTabs === 1 ? 'text-slate-900' : 'text-slate-600'"
              >
                <i class="bi bi-hourglass-split"></i>
                <p class="font-semibold">So sánh giá</p>
              </span>
            </template>
          </el-tab-pane>

          <el-tab-pane label="Config" :name="2">
            <template #label>
              <span
                class="flex flex-row flex-nowrap items-center gap-2 text-base"
                :class="infoTabs === 2 ? 'text-slate-900' : 'text-slate-600'"
              >
                <i class="bi bi-graph-up"></i>
                <p class="font-semibold">Lịch sử giá</p>
              </span>
            </template>
          </el-tab-pane>

          <el-tab-pane label="Role" :name="3">
            <template #label>
              <span
                class="flex flex-row flex-nowrap items-center gap-2 text-base"
                :class="infoTabs === 3 ? 'text-slate-900' : 'text-slate-600'"
              >
                <i class="bi bi-info-circle"></i>
                <p class="font-semibold">Mô tả sản phẩm</p>
              </span>
            </template></el-tab-pane
          >

          <el-tab-pane label="Task" :name="4">
            <template #label>
              <span
                class="flex flex-row flex-nowrap items-center gap-2 text-base"
                :class="infoTabs === 4 ? 'text-slate-900' : 'text-slate-600'"
              >
                <i class="bi bi-wechat"></i>
                <p class="font-semibold">Đánh giá từ người mua</p>
              </span>
            </template></el-tab-pane
          >
        </el-tabs>
      </div>

      <PriceCompare />

      <el-divider />

      <HistoryPrice />

      <el-divider />

      <ProductDescription />

      <el-divider />

      <Evaluate />

      <RelatedProduct />

      <Suggest />

      <el-divider />

      <Blog />

      <el-divider />

      <SuggestionToday />
    </section>
  </main>

  <div class="w-full h-1 mt-10 bg-[#FF7227]"></div>

  <footer class="flex justify-center py-12">
    <div class="w-[1024px] grid grid-cols-3 gap-2">
      <div class="p-4">
        <img
          src="https://lh3.googleusercontent.com/pw/ADCreHe1uaXgFtO8dlQi1fSrqmcu7OPYJYtSDgXclZin8jZ7oMkHSNc20AqAt7f3wnxrneK1VtZe0s9R7e2476DKCTes06oqHbdx41zz-o15Nf9ggs3HHqGC2K8Ym-dgGvem2sd_03jB8KlUf2MDyq4GOTH_=w256"
          alt=""
        />
        <p class="mt-3">
          Mua Thông Minh là website, ứng dụng tìm kiếm và đánh giá hàng hóa sản
          phẩm online. Giúp bạn né Sale ảo, mua giá tốt, tin cậy và trở thành
          người tiêu dùng thông thái. MuaThongMinh.vn không bán hàng!
        </p>
        <p class="mt-3 text-base uppercase">Kết Nối với chúng tôi</p>

        <ul class="mt-3 flex flex-row flex-nowrap items-center gap-4 text-xl">
          <li><i class="bi bi-facebook"></i></li>
          <li><i class="bi bi-instagram"></i></li>
          <li><i class="bi bi-github"></i></li>
        </ul>
      </div>

      <div class="p-4">
        <p class="mb-4 text-lg font-medium uppercase">Về mua thông minh</p>

        <ul class="grid grid-cols-1 gap-4">
          <li>Blog</li>
          <li>Giới thiệu</li>
          <li>Chinh sách bảo mật</li>
          <li>Điều khoản sử dụng</li>
          <li>Metric</li>
          <li>Điểm thi</li>
        </ul>
      </div>

      <div class="p-4">
        <p class="mb-4 text-lg font-medium uppercase">Liên hệ</p>
        <ul class="grid grid-cols-1 gap-1">
          <li>Công ty Cổ phần Khoa học Dữ liệu</li>
          <li>Số ĐKKD: 0108677693</li>
          <li>
            Địa chỉ: Tầng 6 toà nhà AZ Lâm Viên, 107A Nguyễn Phong Sắc, Phường
            Dịch Vọng Hậu, Quận Cầu Giấy, Thành phố Hà Nội, Việt Nam.
          </li>
          <li>Email: info@beecost.com</li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
#product_info_tab {
  .el-tabs__active-bar {
    background-color: #ea4c11;
  }
}
</style>
