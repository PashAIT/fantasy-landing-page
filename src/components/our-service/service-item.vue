<template>
  <div class="serviceItem column items-center justify-center">
    <img src="images/uiux.svg" alt="ui ux icon" class="q-mb-lg" />
    <h3 class="q-mb-lg">UI/UX Design</h3>
    <p>
      We take solo projects for design, as well as develop the designs of the
      websites.
    </p>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';

.serviceItem {
  padding: 42px 28px;
  background: #ffffff;
  border-radius: 50px;
  font-style: normal;
  @include afterNotebook {
    padding: 25px 24px;
  }
  h3 {
    color: #070707;
    font-weight: 600;
    font-size: 40px;
    line-height: 48px;
    @include afterNotebook {
      font-size: 2.792vw;
      margin-bottom: 10px;
    }
  }
  p {
    font-weight: 400;
    font-size: 25px;
    line-height: 30px;
    text-align: center;
    letter-spacing: -0.025em;
    margin: 0;
    @include afterNotebook {
      font-size: 18px;
      line-height: 22px;
    }
  }
}
</style>
