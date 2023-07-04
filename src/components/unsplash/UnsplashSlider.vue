<template>
  <div className="unsplash__slider">
    <Swiper
      class="Swiper"
      effect="coverflow"
      :modules="modules"
      :slides-per-view="5"
      :space-between="50"
      navigation
      :pagination="{ clickable: true }"
      :autoplay="{
        delay: 1000,
        disableOnInteraction: false,
      }"
      :loop="true"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      }"
    >
      <SwiperSlide v-for="(unsplash, index) in unsplashs" :key="index">
        <a
          :href="`https://unsplash.com/search/photos/${unsplash.id}`"
          target="_blank"
          rel="noreferrer"
        >
          <img :src="unsplash.urls.small" :alt="unsplash.original_title" />
        </a>
      </SwiperSlide>
      <div class="swiper-pagination"></div>
      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </Swiper>
  </div>
</template>
<script>
import {
  Navigation,
  Pagination,
  Scrollbar,
  A11y,
  Autoplay,
  EffectCoverflow,
} from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
export default {
  props: {
    unsplashs: {
      type: Array,
      require: true,
    },
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [
        Navigation,
        Pagination,
        Scrollbar,
        A11y,
        Autoplay,
        EffectCoverflow,
      ],
    };
  },
};
</script>
<style lang="scss">
.unsplash__slider {
  width: 100%;
  margin-bottom: 100px;
  .Swiper {
    width: 100%;
    height: 100%; /* 높이를 100%로 설정하여 화면에 맞게 조정합니다 */
    padding: 20px 0 50px;
    img {
      margin: auto;
      height: 300px;
      object-fit: cover;
    }
    .swiper-button-next,
    .swiper-button-prev {
      display: none;
    }
  }
}
</style>
