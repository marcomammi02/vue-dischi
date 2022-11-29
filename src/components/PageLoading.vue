<template>
  <div class="loader">
    <font-awesome-icon icon="fa-solid fa-spinner" class="spinner"/>
  </div>
</template>

<script>
export default {
  name: 'PageLoading',
};
</script>

<style>
  .spinner{
    font-size: 5rem;
    color: #726e6a;
    position: absolute;
    top: 50%;
    left: 50%;
    animation: rotation 1.5s infinite;
  }

  @keyframes rotation {
  100% {transform: rotate(360deg);}
  }
</style>
