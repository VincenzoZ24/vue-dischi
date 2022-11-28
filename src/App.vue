<template>
  <div class="container">
    <HeaderPage />
    <MainPage />
    <CardSongs />
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';
import CardSongs from '@/components/CardSongs.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
    CardSongs,
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
