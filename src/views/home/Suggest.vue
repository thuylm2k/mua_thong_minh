<template>
  <div class="mt-6">
    <p class="text-lg font-semibold">Gợi ý dành cho bạn</p>

    <div class="mt-3">
        <Carousel :items-to-show="4.5" :wrap-around="true" :itemsToScroll="2">
        <Slide v-for="(item, index) in 10" :key="index">
          <SugProductBox />
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
      
    </div>
  </div>
</template>

<script >
import { defineComponent } from "vue";
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
import SugProductBox from "../../components/SugProductBox.vue";

export default defineComponent({
  name: "RelatedProduct",
  components: {
    SugProductBox,
    Carousel,
    Slide,
    Navigation,
  },
});
</script>

<style lang="scss" scoped></style>
