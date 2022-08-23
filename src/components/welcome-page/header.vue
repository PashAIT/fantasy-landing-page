<template>
  <div class="header row full-width justify-between items-center">
    <nav class="col-9 justify-end items-center flex">
      <ul class="row">
        <li
          v-for="item in navItems"
          :key="`item${item.id}`"
          class="cursor-pointer"
          style="list-style-type: none; color: #fff"
        >
          {{ item.title }}
        </li>
      </ul>
      <div class="hidden-menu-icon">
        <div
          id="nav-icon4"
          :class="{ open: hiddenMenu }"
          @click="openHiddenMenu"
        >
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </nav>
    <div class="ait col-2 row items-center">
      <img src="images/Ait.svg" alt="" />
    </div>
    <q-dialog v-model="hiddenMenu" position="right" class="hidden-menu">
      <q-card
        class="modal-content"
        style="
          width: 64vw;
          max-width: 90vw;
          height: 100vh;
          max-height: fit-content;
        "
      >
        <ul class="column">
          <li
            v-for="item in navItems"
            :key="`item${item.id}`"
            class="cursor-pointer"
            style="list-style-type: none; color: #fff"
          >
            {{ item.title }}
          </li>
        </ul>
      </q-card>
    </q-dialog>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

interface INav {
  id: number;
  title: string;
  path: string;
}
let hiddenMenu = ref(false);
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

//methods
function openHiddenMenu(): void {
  hiddenMenu.value = !hiddenMenu.value;
}
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.header {
  padding: 54px 7.2vw 0;
  margin-bottom: 16.6vh;

  @include tablet {
    flex-direction: row-reverse;
  }
  @include mobile {
    padding-top: 47px;
  }
  nav {
    position: relative;
    z-index: 10000;
    ul {
      @include tablet {
        display: none;
      }
      @include noteBook {
        :last-child {
          margin-right: 0;
        }
      }
      li {
        font-style: normal;
        font-weight: 500;
        font-size: 1.5rem;
        line-height: 29px;
        margin-right: 2.8vw;
        @include noteBook {
          font-size: 22px;
        }
      }
    }
    img {
      display: none;
      @include tablet {
        display: block;
      }
    }
    .hidden-menu-icon {
      width: 50px;
      height: 50px;
      background: #fff;
      border-radius: 100%;
      display: none;
      z-index: 10;

      #nav-icon4 {
        width: 60px;
        height: 45px;
        position: relative;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: 0.5s ease-in-out;
        -moz-transition: 0.5s ease-in-out;
        -o-transition: 0.5s ease-in-out;
        transition: 0.5s ease-in-out;
        cursor: pointer;
      }

      #nav-icon4 span {
        display: block;
        position: absolute;
        height: 4px;
        width: 40%;
        background: #000000;
        border-radius: 9px;
        opacity: 1;
        left: 13px;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: 0.25s ease-in-out;
        -moz-transition: 0.25s ease-in-out;
        -o-transition: 0.25s ease-in-out;
        transition: 0.25s ease-in-out;
      }
      #nav-icon4 span:nth-child(1) {
        top: 14px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4 span:nth-child(2) {
        top: 23px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4 span:nth-child(3) {
        top: 32px;
        -webkit-transform-origin: left center;
        -moz-transform-origin: left center;
        -o-transform-origin: left center;
        transform-origin: left center;
      }

      #nav-icon4.open span:nth-child(1) {
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        transform: rotate(47deg);
        top: 14px;
        left: 16px;
      }

      #nav-icon4.open span:nth-child(2) {
        width: 0%;
        opacity: 0;
      }

      #nav-icon4.open span:nth-child(3) {
        -webkit-transform: rotate(-45deg);
        -moz-transform: rotate(-45deg);
        -o-transform: rotate(-45deg);
        transform: rotate(-52deg);
        top: 32px;
        left: 17px;
      }
      @include tablet {
        display: block;
      }

      q-btn {
        border-radius: 100%;
      }
    }
  }
  .ait {
    position: relative;
    @include tablet {
      img {
        width: 121px;
        height: 55px;
      }
    }
    @include mobile {
      img {
        width: 100px;
        height: 44px;
      }
    }
  }
}
.hidden-menu {
  z-index: 9 !important;
  .modal-content {
    padding: 24vh 7.2vw 9.15625vw;
    backdrop-filter: blur(4px);
    background: rgba(63, 15, 123, 0.67);
    ul {
      :first-child {
        margin-top: 0;
      }
      li {
        font-style: normal;
        font-weight: 500;
        font-size: 6.25vw;
        line-height: 60px;
        margin-top: 5vw;

        @include mobile {
          font-size: 32px;
          line-height: 38px;
        }
      }
    }
  }
}
</style>
