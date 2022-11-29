<template>
  <div class="main">
    <div class="card-container mx-auto">
      <ul v-if="arrDischi" class="row row-cols-5 g-3">
        <PageCard v-for="objDisco in arrDischi" :key="objDisco.author"
        :imgUrl="objDisco.poster"
        :title="objDisco.title"
        :author="objDisco.author"
        :year="objDisco.year"
    />
      </ul>
      <div v-else><PageLoading /></div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import PageCard from '@/components/PageCard.vue';
import PageLoading from '@/components/PageLoading.vue';

export default {
  name: 'PageMain',
  components: {
    PageCard,
    PageLoading,
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
      });
  },
};
</script>

<style>
  .card-container {
    max-width: 800px;
    margin-top: 3rem;

  }
</style>
