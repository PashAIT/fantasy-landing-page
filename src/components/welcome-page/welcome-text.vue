<template>
  <div class="welcome-text column justify-center items-center">
    <h1 class="q-mb-md column items-center">
      Fantasy <span> space for unlimited minds</span>
    </h1>
    <p class="q-mb-xl">
      Fantasy is an IT company based in Armenia, specializing in developing Web
      and Mobile applications.
      <span
        >Valuing customization and individual approach towards its partners, it
        provides services and solutions that make businesses visible in the
        digital space</span
      >
    </p>
    <q-btn
      unelevated
      rounded
      label="See More"
      no-caps
      class="see-more-button"
    />
  </div>
</template>

<script lang="ts" setup></script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';

.welcome-text {
  width: 61.3020833333vw;
  @include afterNotebook {
    width: 70vw;
  }
  @include tablet {
    width: 79vw;
  }
  z-index: 1;
  h1 {
    font-style: normal;
    font-weight: 700;
    text-align: center;
    font-size: 8.75rem;
    line-height: 90%;
    // @include afterNotebook {
    //   font-size: 120px;
    // }
    @include noteBook {
      font-size: 6.25rem;
      margin-bottom: 0.9vw;
    }
    // @include tablet {
    //   font-size: 12.5vw;
    // }
    @include mobile {
      font-size: 3.43rem;
    }
    span {
      font-size: 4.6vw;
      @include afterNotebook {
        font-size: 68px;
      }
      @include noteBook {
        font-size: 48px;
      }
      @include tablet {
        font-size: 6vw;
      }
      @include mobile {
        font-size: 22px;
      }
    }
  }
  p {
    width: 90%;
    text-align: center;
    font-style: normal;
    font-weight: 400;
    font-size: 1.5rem;
    line-height: 122.7%;
    // @include afterNotebook {
    //   font-size: 22px;
    // }
    // @include noteBook {
    //   font-size: 20px;
    // }
    @include tablet {
      font-size: 0.93rem;
      margin-bottom: 35px;
    }
    // @include mobile {
    //   font-size: 15px;
    // }
    span {
      font-size: 1.5rem;
      @include tablet {
        display: none;
      }
    }
  }
  .see-more-button {
    font-family: 'Barlow Semi Condensed', sans-serif;
    padding: 18px 47px;
    font-weight: 600;
    font-size: 2rem !important;
    line-height: 122.7%;
    background: linear-gradient(180deg, #6b71f1 0%, #7216c4 100%);
    @include noteBook {
      padding: 0 30px;
    }
    @include noteBook {
      font-size: 20px;
    }
    @include mobile {
      font-size: 16px;
    }
  }
}
</style>
