<template>
  <ContTitle title="unsplash" />
  <UnsplashSlider :unsplashs="unsplashs" />
  <UnsplashSearch />
  <UnsplashTag />
  <UnsplashCont :unsplashs="unsplashs" />
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },

  setup() {
    const unsplashs = ref([]);

    const TopUnsplash = async () => {
      await fetch(
        "https://api.unsplash.com/photos?client_id=Y5YRP4enZkTmKiGv73DRLR4X1vXjLibm7fCZg_Y45_8&per_page=30"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          unsplashs.value = result;
        })
        .catch((error) => console.log("error", error));
    };
    TopUnsplash();

    return {
      unsplashs,
      TopUnsplash,
    };
  },
};
</script>
