<template>
  <div class="container">
    <HeaderPage />
    <MainPage :selectedValue="selectedValue"/>

  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  name: 'App',
  data() {

  },
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
