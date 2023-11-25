<template>
  <div class="mt-5">
    <p class="text-lg font-semibold">Sản phẩm liên quan</p>

    <div>
      <Carousel :items-to-show="4.5" :wrap-around="true" :itemsToScroll="2">
        <Slide v-for="(item, index) in 10" :key="index">
          <BoxProduct />
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
import BoxProduct from "../../components/BoxProduct.vue";

export default defineComponent({
  name: "RelatedProduct",
  components: {
    BoxProduct,
    Carousel,
    Slide,
    Navigation,
  },
});
</script>

<style lang="scss" scoped></style>
