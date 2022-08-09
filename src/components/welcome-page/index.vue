<template>
  <video autoplay muted playsinline loop id="myVideo">
    <source src="video/AdorableLonelyKilldeer-mobile.mp4" type="video/mp4" />
  </video>
  <div
    class="welcome-page column items-center full-width"
    style="height: 100vh"
  >
    <Header />
    <welcome-text />
  </div>
</template>

<script setup lang="ts">
import Header from './header.vue';
import WelcomeText from './welcome-text.vue';
</script>

<style lang="scss" scoped>
#myVideo {
  position: absolute;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
}
.welcome-page {
  background: rgba(0, 0, 0, 0.5);
  color: #f1f1f1;
  width: 100%;
  margin-bottom: 150px;
}
</style>
