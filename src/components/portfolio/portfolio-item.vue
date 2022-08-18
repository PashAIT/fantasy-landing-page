<template>
  <div>
    <q-img
      :src="props.item.img"
      spinner-color="white"
      img-class="my-custom-image"
      style="border-radius: 27px"
      @mouseover="showText = true"
      @mouseleave="showText = false"
    >
      <div
        v-show="showText"
        class="absolute-right text-subtitle1 text-center"
        style="border-radius: 40px 0px 0px 40px"
      >
        Caption
      </div>
    </q-img>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';
const props = defineProps({
  item: Array,
});
console.log(props.item);
let showText = ref(false);
</script>

<style lang="scss" scoped></style>
