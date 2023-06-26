<template>
  <div className="unsplash__cont container">
    <ul>
      <li v-for="(unsplash, index) in unsplashs" :key="index">
        <a :href="`https://unsplash.com/photos/${unsplash.id}`">
          <img :src="unsplash.urls.regular" :alt="unsplash.alt_description"
        /></a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    unsplashs: {
      type: Array,
      required: true,
    },
  },
};
</script>
