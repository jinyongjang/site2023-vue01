<template>
  <ContTitle title="youtube" />
  <YoutubeSlider />
  <YoutubeSearch />
  <YoutubeTag />
  <YoutubeCont :youtubes="youtubes" />
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    YoutubeSlider,
    YoutubeSearch,
    YoutubeTag,
    YoutubeCont,
  },

  setup() {
    const youtubes = ref([]);

    const TopYoutube = async () => {
      await fetch(
        "https://www.googleapis.com/youtube/v3/videos?part=snippet&chart=mostPopular&maxResults=27&key=AIzaSyAi3oS-PQt8OVW6Njn4l4CEXeK8m8W-fMQ"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          youtubes.value = result.items;
        })
        .catch((error) => console.log("error", error));
    };
    TopYoutube();

    return {
      youtubes,
      TopYoutube,
    };
  },
};
</script>
