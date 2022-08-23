<template>
  <div class="contact column items-center">
    <h3 class="q-mb-lg">Collaborate with us!</h3>
    <p class="text-center q-mb-xl">
      There are many variations of passages of Lorem Ipsum available, but the
      majority have suffered.
    </p>
    <div class="inputs row justify-center items-center q-col-gutter-x-md">
      <q-input
        ref="nameRef"
        outlined
        v-model="userName"
        label="Your name *"
        lazy-rules
        :rules="[(val) => (val && val.length > 0) || 'Please type something']"
        class="col-md-6 col-xs-12"
      />

      <q-input
        ref="phoneRef"
        outlined
        type="text"
        v-model="userPhone"
        label="Your number *"
        lazy-rules
        :rules="[
          (val) => (val !== null && val !== '') || 'Please type your number',
          (val) => (val > 0 && val < 100) || 'Please type a real number',
        ]"
        class="col-md-6 col-xs-12"
      />
      <q-input
        ref="questionRef"
        outlined
        type="text"
        v-model="userQuestion"
        label="Your number *"
        lazy-rules
        :rules="[(val) => (val && val.length > 0) || 'Please type something']"
        class="col-md-12 col-xs-12"
      >
        <template v-slot:append>
          <q-icon name="img:images/send-icon.svg" /> </template
      ></q-input>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

let nameRef = ref('null');
let userName = ref('');

let phoneRef = ref('');
let userPhone = ref('');

let questionRef = ref('null');
let userQuestion = ref('');
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.contact {
  background: $bgPrimary;
  border-radius: 70px;
  padding: 70px 40px;
  color: white;
  margin-bottom: $marginComponents;
  @include noteBook {
    border-radius: 60px;
  }
  @include tablet {
    border-radius: 50px;
  }
  @include mobile {
    border-radius: 40px;
  }
  @include mobile {
    padding: 60px 13px;
  }
  h3 {
    font-style: normal;
    font-weight: 900;
    font-size: 6.1rem;
    line-height: 151px;
    display: flex;
    align-items: center;
    text-align: center;
    @include afterNotebook {
      font-size: 4.9rem;
      line-height: 120px;
    }
    @include noteBook {
      font-size: 3.3rem;
      line-height: 80px;
    }
    @include mobile {
      font-size: 2.5rem;
      line-height: 48px;
    }
  }
  p {
    max-width: 50%;
    font-style: normal;
    font-weight: 700;
    font-size: 1.25rem;
    line-height: 122.7%;
    @include noteBook {
      max-width: 80%;
      font-size: 1rem;
    }
    @include mobile {
      font-size: 0.7rem;
    }
  }
  .inputs {
    width: 50%;
    @include noteBook {
      width: 80%;
    }
  }
}
</style>
