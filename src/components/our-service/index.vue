<template>
  <div class="service-content column justify-center items-center">
    <h2>Our Service</h2>
    <div
      class="service q-col-gutter-xl row justify-center q-mt-none q-ml-none gt-sm"
    >
      <div v-for="(item, i) in 5" :key="i" class="col-4">
        <service-item />
      </div>
    </div>
    <div class="lt-md full-width">
      <q-carousel
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        swipeable
        animated
        control-color="primary"
        navigation
        class="bg-grey-1 rounded-borders items-slider2"
      >
        <q-carousel-slide :name="1" class="column no-wrap">
          <div
            class="row fit justify-start items-center q-gutter-md q-col-gutter no-wrap"
          >
            <service-item />
            <service-item />
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" class="column no-wrap">
          <div
            class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <service-item />
            <service-item />
          </div>
        </q-carousel-slide>
      </q-carousel>
      <q-carousel
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        swipeable
        animated
        control-color="primary"
        navigation
        class="bg-grey-1 rounded-borders items-slider1"
      >
        <q-carousel-slide :name="1" class="column no-wrap">
          <div
            class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <service-item />
          </div>
        </q-carousel-slide>
        <q-carousel-slide :name="2" class="column no-wrap">
          <div
            class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
          >
            <service-item />
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
</template>

<script setup>
import serviceItem from './service-item.vue';
import { ref } from '@vue/reactivity';

let slide = ref(1);
// let services = ref([
//   {
//     id: 1,
//     title: 'Web',
//     description: 'lorem',
//   },
//   {
//     id: 2,
//     title: 'Web',
//     description: 'lorem',
//   },
// ]);
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.service-content {
  margin-bottom: 350px;
}
.service {
  background: linear-gradient(108.86deg, #00002b 33.23%, #4c128b 93.85%);
  border-radius: 85px;
  padding: 0 48px 48px 0;
  margin-bottom: 350px;
}
.items-slider2 {
  @include mobile {
    display: none;
  }
}
.items-slider1 {
  display: none;
  @include mobile {
    display: block;
  }
}
</style>
