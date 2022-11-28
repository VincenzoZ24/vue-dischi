<template>
<div class="content_song">
    <img class="img_song" :src="poster" alt="">
    <h2>
        {{title}}
    </h2>
    <h4>{{author}}</h4>
    <div>{{year}}</div>
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
.content_song{
    width: calc((1000px - 8rem) / 5);
    .img_song{
        width: 100%;
    }
}
</style>
