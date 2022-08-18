<template>
  <div
    class="founder-item column justify-center items-center"
    style="padding: 5vw 5.2vw 3vw"
  >
    <q-img :src="founder.image" spinner-color="black" class="img" />
    <h3 class="flex items-center">{{ founder.title }}</h3>
    <h4>{{ founder.subTitle }}</h4>
    <div class="icons row full-width justify-center">
      <q-btn
        padding="md"
        color="white"
        icon="img:images/LinkedIn.svg"
        style="border-radius: 15px; height: max-content"
        class="linkedin"
      />
      <q-btn
        padding="md"
        style="border-radius: 15px; height: max-content"
        color="white"
        class="facebook"
        icon="img:images/Facebook.svg"
      />
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps({
  founder: Object,
});
console.log(props.founder);
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.founder-item {
  color: #fff;
  background: linear-gradient(159.11deg, #00002b 13.81%, #4c128b 98.63%);
  border-radius: 70px;
  @include noteBook {
    border-radius: 50px;
  }

  .img {
    margin-bottom: 40px;
    border-radius: 56px;
    @include tablet {
      border-radius: 20px;
      margin-bottom: 20px;
    }
  }
  h3 {
    font-style: normal;
    font-weight: 600;
    font-size: 2.4vw;
    line-height: 60px;
    margin-bottom: 8px;
    text-transform: capitalize;
    @include noteBook {
      line-height: 40px;
      font-size: 3vw;
      magin: 0;
    }
    @include tablet {
      line-height: 30px;
      font-size: 18px;
    }
  }
  h4 {
    font-style: normal;
    font-weight: 600;
    font-size: 1.8vw;
    line-height: 42px;
    text-transform: capitalize;
    margin-bottom: 25px;
    @include noteBook {
      font-size: 2.2vw;
      line-height: 22px;
      margin-bottom: 2.1vw;
    }
    @include tablet {
      line-height: 18px;
      margin-bottom: 17px;
      font-size: 17px;
    }
  }
  .icons {
    .linkedin {
      margin-right: 2.86458333333vw;
    }
    q-btn {
      @include tablet {
        padding: 8px;
      }
    }
  }
}
</style>
