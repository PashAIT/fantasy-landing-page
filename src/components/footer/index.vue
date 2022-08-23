<template>
  <div class="footer row justify-between items-center q-col-gutter-x-md">
    <img
      src="images/footer-logo.svg"
      alt="footer logo"
      class="col-md-2 col-xs-3"
    />
    <ul class="col-md-7 row justify-between items-center">
      <li
        v-for="item in navItems"
        :key="`item${item.id}`"
        class="cursor-pointer col-2"
        style="list-style-type: none; color: #fff"
      >
        {{ item.title }}
      </li>
    </ul>
    <div class="icons col-md-2 col-xs-3">
      <div class="row items-center justify-center">
        <q-icon name="img:images/footer-fb.svg" class="col-2" />
        <q-icon name="img:images/footer-be.svg" class="col-2" />
        <q-icon name="img:images/footer-linkedIn.svg" class="col-2" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { INav } from '../models';

const navItems = ref<INav[]>([
  {
    id: 1,
    title: 'Home',
    path: '#',
  },
  {
    id: 2,
    title: 'Service',
    path: '#our-service',
  },
  {
    id: 3,
    title: 'Founders',
    path: '#founders',
  },
  {
    id: 4,
    title: 'Portfolio',
    path: '#portfolio',
  },
  {
    id: 5,
    title: 'Contact',
    path: '#contact',
  },
]);
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.footer {
  padding: 43px 120px;
  background: $bgPrimary;
  border-radius: 70px 70px 0px 0px;
  @include noteBookxs {
    padding: 25px;
    border-radius: 40px 40px 0px 0px;
  }
  ul {
    margin-top: 1%;
    @include noteBookxs {
      display: none;
    }
    li {
      font-style: normal;
      font-weight: 500;
      font-size: 1.8vw;
      line-height: 42px;
    }
  }
  .icons {
    span {
      margin-right: 10px;
    }
  }
}
</style>
