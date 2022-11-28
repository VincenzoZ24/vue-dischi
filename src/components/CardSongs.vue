<template>
  <div class="content_song">
    <img class="img_song" :src="poster" alt="" />
    <h2>
      {{ title }}
    </h2>
    <div class="autore_anni">
      <h4>{{ author }}</h4>
      <div>{{ year }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardSongs',
  props: {
    poster: String,
    title: String,
    author: String,
    genre: String,
    year: String,
  },
};
</script>

<style lang="scss" scoped>
.content_song {
  width: calc((1000px - 8rem) / 5);
  align-self: flex-start;
  padding: 1rem;
  align-self: stretch;
  background-color: rgba(46, 58, 70, 1);
  text-align: center;
  color: white;

  .img_song {
    width: 100%;
  }
}
h2 {
  margin-top: 1rem;
}
.autore_anni{
    color: rgba(113, 115, 118, 1);
    font-size: 12px;
    margin-top: 2rem;
}
</style>
