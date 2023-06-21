<template>
  <main>
    <SliderSection attr="slider__wrap section gmarket5" />
    <IntroSection attr="intro__wrap section bg-blue" />
    <PortSection attr="port__wrap section center" />
    <YoutubeSection attr="youtube__wrap gmarket5 section bg-blue" />
    <UnsplashSection attr="unsplash__wrap gmarket5 section" />
    <MovieSection attr="movies__wrap section bg-blue" />
  </main>
</template>

<script>
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";

export default {
  components: {
    SliderSection,
    IntroSection,
    PortSection,
    MovieSection,
    YoutubeSection,
    UnsplashSection,
  },
};
</script>
