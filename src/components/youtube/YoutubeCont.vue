<template>
  <div className="youtube__cont container">
    <ul>
      <li v-for="(youtube, index) in youtubes" :key="index">
        <img :src="youtube.snippet.thumbnails.medium.url" alt="youtube" />
        <span>{{ youtube.snippet.title }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>
