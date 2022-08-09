<template>
  <div class="column justify-center items-center">
    <h2>Our Service</h2>
    <div
      class="service q-col-gutter-xl row justify-center q-mt-none q-ml-none gt-sm"
    >
      <div v-for="(item, i) in 5" :key="i" class="col-4">
        <service-item />
      </div>
    </div>
    <div class="lt-md">
      <div id="q-app" style="min-height: 100vh">
        <div class="q-pa-md">
          <q-carousel
            v-model="slide"
            transition-prev="slide-right"
            transition-next="slide-left"
            swipeable
            animated
            control-color="primary"
            navigation
            padding
            arrows
            height="500px"
            class="bg-grey-1 shadow-2 rounded-borders"
          >
            <q-carousel-slide :name="1" class="column no-wrap">
              <div
                class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
              >
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/mountains.jpg"
                ></q-img>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/parallax1.jpg"
                ></q-img>
              </div>
            </q-carousel-slide>
            <q-carousel-slide :name="2" class="column no-wrap">
              <div
                class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
              >
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/parallax2.jpg"
                ></q-img>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/quasar.jpg"
                ></q-img>
              </div>
            </q-carousel-slide>
            <q-carousel-slide :name="3" class="column no-wrap">
              <div
                class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
              >
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/cat.jpg"
                ></q-img>
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/linux-avatar.png"
                ></q-img>
              </div>
            </q-carousel-slide>
            <q-carousel-slide :name="4" class="column no-wrap">
              <div
                class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
              >
                <q-img
                  class="rounded-borders col-6 full-height"
                  src="https://cdn.quasar.dev/img/material.png"
                ></q-img>
              </div>
            </q-carousel-slide>
          </q-carousel>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import serviceItem from './service-item.vue';
</script>

<style lang="scss" scoped>
.service {
  background: linear-gradient(108.86deg, #00002b 33.23%, #4c128b 93.85%);
  border-radius: 85px;
  padding: 0 48px 48px 0;
  margin-bottom: 350px;
}
</style>
