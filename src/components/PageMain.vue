<template>
  <div class="main">
    <div class="card-container">
      <ul v-if="arrDischi" class="row row-cols-5 g-3">
        <PageCard v-for="objDisco in arrDischi" :key="objDisco.author"
        :imgUrl="objDisco.poster"
        :title="objDisco.title"
        :author="objDisco.author"
        :year="objDisco.year"
    />
      </ul>
      <div v-else>Loading...</div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import PageCard from '@/components/PageCard.vue';

export default {
  name: 'PageMain',
  components: {
    PageCard,
  },

  data() {
    return {
      arrDischi: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },

  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        this.arrDischi = axiosResponse.data.response;
        console.log(this.arrDischi);
        console.log(this.arrDischi[0].author);
      });
  },
};
</script>

<style>
  .main {
    background-color: #1e2d3b;

    z-index: -1;
  }

  .card-container {
    max-width: 900px;

  }
</style>
