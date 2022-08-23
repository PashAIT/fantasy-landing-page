<template>
  <div>
    <welcome-page />
    <div class="content row items-center justify-center">
      <Service class="col-12" />
      <Founders class="col-12" />
      <Portfolio class="col-12" />
      <Contact class="col-11" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import WelcomePage from 'src/components/welcome-page';
import Service from 'src/components/our-service';
import Founders from 'src/components/founders';
import Portfolio from 'src/components/portfolio';
import Contact from './components/contact/index.vue';
</script>
<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  // font-family: 'Barlow Semi Condensed', sans-serif;
  // font-family: 'Montserrat', sans-serif;
  font-family: 'Recursive', sans-serif;
}
.content {
  padding: 0 7.29166666667vw;
}
</style>
