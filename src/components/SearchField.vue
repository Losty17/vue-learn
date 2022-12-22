<template>
  <div class="search">
    <img src="../assets/search.svg">
    <input type="text" placeholder="Insira ou busque um link" @input="handleSearch">
  </div>
</template>

<script>
export default {
  name: 'SearchField',
  props: {
    handleSearch: {
      type: Function,
      default: () => {}
    }
  }
}
</script>

<style scoped>
.search {
  height: 48px;
  border: 2px solid #fff;
  border-radius: 24px;
  padding: 20px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  transition: 500ms;
  margin-bottom: 72px;
}

.search > img {
  height: 24px;
}

.search > input {
  background: transparent;
  border: none;
  outline: none;
  color: #fff;
  font-size: 18px;
  margin-left: 12px;
  width: 100%;
}

.search > input::placeholder {
  color: #fff;
  opacity: 0.5;
}
</style>