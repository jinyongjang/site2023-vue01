<template>
  <section class="movie__slider">
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
      <SwiperSlide v-for="(movie, index) in movies" :key="index">
        <a target="_blank" rel="noreferrer">
          <img
            :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`"
            :alt="movie.title"
          />
        </a>
      </SwiperSlide>
      <div class="swiper-pagination"></div>
      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </Swiper>
  </section>
</template>

<script>
import {
  Navigation,
  // Pagination,
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
    movies: {
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
        // Pagination,
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
.movie__slider .swiper {
  padding-bottom: 50px;
  text-align: center;
  justify-content: center;
  display: block;
}
.movie__slider .swiper img {
  width: 100%;
  display: inline;
}
</style>
