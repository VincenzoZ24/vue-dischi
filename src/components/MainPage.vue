<template>
  <div class="container">
    <CardSongs
      v-for="card in arrSongs"
      :key="card.poster"
      :poster="card.poster"
      :title="card.title"
      :author="card.author"
      :year="card.year"
    />
  </div>
</template>

<script>
import axios from 'axios';
import CardSongs from '@/components/CardSongs.vue';

export default {
  name: 'MainPage',
  components: {
    CardSongs,
  },
  data() {
    return {
      arrSongs: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlApi).then((axiosResponse) => {
      this.arrSongs = axiosResponse.data.response;
    });
  },
};
</script>

<style lang="scss" scoped>
.container {
  background-color: rgba(30, 45, 59, 1);

}
</style>
