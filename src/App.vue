<template>
  <div>
    <PageHeader />
    <PageMain />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader.vue';
import PageMain from '@/components/PageMain.vue';

export default {
  components: {
    PageHeader,
    PageMain,
  },
};
</script>

<style>
  @import 'bootstrap';

  * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

  body {
    background-color: #1e2d3b;
  }

</style>
