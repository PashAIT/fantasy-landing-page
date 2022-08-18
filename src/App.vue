<template>
  <div>
    <welcome-page />
    <div class="content">
      <Service />
      <Founders />
      <Portfolio />
    </div>
  </div>
</template>

<script lang="ts" setup>
import WelcomePage from 'src/components/welcome-page';
import Service from 'src/components/our-service';
import Founders from 'src/components/founders';
import Portfolio from 'src/components/portfolio';
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
