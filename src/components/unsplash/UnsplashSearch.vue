<template>
  <div class="unsplash-search container">
    <h2 class="blind">검색하기</h2>
    <input
      class="input"
      ref="inputRef"
      type="search"
      @keydown.enter="handleSearch"
      placeholder="이미지를 검색하세요!"
    />
    <button type="submit" @click="handleSearch">검색하기</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputRef: null,
    };
  },
  mounted() {
    this.inputRef = this.$refs.inputRef;
  },
  methods: {
    handleSearch() {
      const value = this.inputRef.value;
      this.$emit("search", value);
    },
  },
};
</script>

<style scoped>
.unsplash-search {
  text-align: center;
  margin-bottom: 50px;
}
.input {
  border: 1px solid #e8ecf2;
  font-size: 16px;
  padding: 10px 20px;
  border-radius: 50px;
  min-width: 300px;
  margin-right: 10px;
  font-family: "GmarketSans";
}
.unsplash-search button {
  background-color: #4857ec;
  color: #fff;
  border: none;
  border-radius: 50px;
  font-size: 16px;
  padding: 10px 20px;
  font-family: "GmarketSans";
}
</style>
