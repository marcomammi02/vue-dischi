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
    height: 220px;
  }

  img {
    width: 110px;
    margin-top: 15px
  }

  .title {
    color: #ffffff;
    font-size: 1rem;
    margin: 10px 0 0;
  }

  p {
    color: #726e6a;
    margin: 0;
    font-size: .9rem;
  }
</style>
