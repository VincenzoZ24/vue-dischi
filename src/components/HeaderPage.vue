<template>
  <div class="bar_header">
    <SelectCard/>
  </div>
</template>

<script>
import SelectCard from '@/components/SelectCard.vue';

export default {
  name: 'HeaderPage',
  components: {
    SelectCard,
  },
};
</script>

<style lang="scss" scoped>
.bar_header {
  background-color: rgba(46, 58, 70, 1);
  height: 4rem;
}
</style>
