<template>
  <div>
    <welcome-page />
    <div class="content">
      <Service />
    </div>
  </div>
</template>

<script lang="ts" setup>
import WelcomePage from 'src/components/welcome-page';
import Service from 'src/components/our-service';
</script>
<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Barlow Semi Condensed', sans-serif;
}
.content {
  padding: 0 7.29166666667vw;
}
</style>
