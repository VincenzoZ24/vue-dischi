<template>
  <div class="container">

    <div class="container_songs">
        <CardSongs
      v-for="card in arrSongs"
      :key="card.poster"
      :poster="card.poster"
      :title="card.title"
      :author="card.author"
      :year="card.year"
      :genre="card.genere"

    />
    </div>

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
  height: 100vh;
  .container_songs{
    max-width: 1000px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    height: 100%;
    align-items: center;
    padding: 3rem 0 ;
  }
}
</style>
