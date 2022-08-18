<template>
  <div class="founders row q-col-gutter-lg justify-evenly">
    <div
      class="col-lg-5 col-md-6 col-sm-6 col-xs-10"
      v-for="item in founders"
      :key="`item${item.id}`"
    >
      <founder-item :founder="item" />
    </div>
  </div>
</template>

<script setup>
import founderItem from 'src/components/founders/founder-item.vue';
import { ref } from '@vue/reactivity';

let founders = ref([
  {
    id: 1,
    title: 'Yervand Tadevosyan',
    subTitle: 'Founder CEO',
    image: 'images/Yervandsvg.svg',
    fbLink: '',
    linkedInLink: '',
  },
  {
    id: 2,
    title: 'Yervand Tadevosyan',
    subTitle: 'Founder CEO',
    image: 'images/Yervandsvg.svg',
    fbLink: '',
    linkedInLink: '',
  },
]);
</script>

<style lang="scss" scoped>
.founders {
  margin-bottom: 350px;
}
</style>
