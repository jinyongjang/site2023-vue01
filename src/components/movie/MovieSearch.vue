<template>
  <div class="movie__search container">
    <h2 class="blind">검색</h2>
    <input
      ref="inputRef"
      type="search"
      @keypress="onKeyPress"
      placeholder="영화를 검색하세요!"
    />
    <button type="submit" @click="onClick">검색</button>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$refs.inputRef.focus();
  },
  methods: {
    handleSearch() {
      const value = this.$refs.inputRef.value;
      this.$emit("search", value);
    },
    onKeyPress(event) {
      if (event.key === "Enter") {
        this.handleSearch();
      }
    },
    onClick() {
      this.handleSearch();
    },
  },
};
</script>

<style lang="scss">
.movie__search {
  text-align: center;
  margin-bottom: 50px;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    border-radius: 50px;
    min-width: 300px;
    margin-right: 10px;
    font-family: "GmarketSans";
  }
  button {
    @include button(#ff0000, #fff);
    border-radius: 50px;
    font-family: "GmarketSans";
  }
}
</style>
