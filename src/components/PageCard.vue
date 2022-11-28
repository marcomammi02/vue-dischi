<template>
  <div class="col">
    <div class="card-box text-center">
      <img :src="imgUrl" :alt="title">
      <h1 class="title">{{ title }}</h1>
      <p class="author">{{ author }}</p>
      <p class="year">{{ year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageCard',
  props: {
    imgUrl: String,
    title: String,
    author: String,
    year: String,
  },
};
</script>

<style scoped>
  .card-box {
    background-color: #2e3a46;
  }

  img {
    width: 50px;
  }
</style>
