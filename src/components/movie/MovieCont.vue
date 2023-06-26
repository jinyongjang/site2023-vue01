<template>
  <div className="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a
          :href="`https://www.themoviedb.org/movie/${movie.id}`"
          target="_blank"
        >
          <img
            :src="`https://image.tmdb.org/t/p/w500${movie.poster_path}`"
            alt="movie.title"
          />
          <em>
            <span className="title">{{ movie.title }}</span>
            <span className="star">{{ movie.vote_average }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>
