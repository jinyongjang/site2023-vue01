<template>
  <div>
    <ContTitle title="movies" />
    <MovieSlider :movies="movies" />
    <MovieSearch @search="searchMovies" />
    <MovieTag />
    <MovieCont :movies="movies" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },

  setup() {
    const movies = ref([]);
    const search = ref("");

    const fetchPopularMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=310e025fb6da176e86a5210874607f40&language=en-US&page=1`
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          movies.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };

    const TopMovies = async () => {
      if (search.value === "") {
        fetchPopularMovies();
      } else {
        await fetch(
          `https://api.themoviedb.org/3/search/movie?api_key=310e025fb6da176e86a5210874607f40&language=en-US&query=${search.value}&page=1&include_adult=true`
        )
          .then((response) => response.json())
          .then((result) => {
            console.log(result);
            movies.value = result.results;
          })
          .catch((error) => console.log("error", error));
      }
    };

    const searchMovies = (value) => {
      search.value = value;
      TopMovies();
    };

    TopMovies();

    return {
      movies,
      searchMovies,
    };
  },
};
</script>
