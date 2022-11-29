<template>
  <div class="container">
    <HeaderPage />
    <MainPage />
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,

  },
};
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  background-color:  rgba(30, 45, 59, 1);
}
</style>
