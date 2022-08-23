<template>
  <div class="portfolio column justify-center items-center">
    <h2>Our Portfolio</h2>
    <div class="full-width">
      <q-tabs
        v-model="tab"
        align="left"
        active-class="activeTab"
        content-class="contentTab"
        class="q-pb-md"
      >
        <q-tab
          v-for="tab in tabs"
          :key="`tab${tab.id}`"
          :name="tab.title"
          :label="tab.title"
        ></q-tab>
      </q-tabs>
      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="All" class="q-pl-none">
          <q-carousel
            v-model="activeCarouselItem"
            transition-prev="scale"
            transition-next="scale"
            swipeable
            animated
            navigation-icon="img:images/carouselNavicon.svg"
            navigation-active-icon="img:images/carouoselActiveicon.svg"
            control-text-color="deep-purple-10"
            navigation
            height="max-content"
            style="padding-bottom: 120px; min-height: 57.1vw"
          >
            <q-carousel-slide
              v-for="(item, i) in carouselItems"
              :key="`item${i}`"
              :name="item.name"
              class="row items-center justify-center q-col-gutter-xl q-pl-none slider-container"
            >
              <portfolio-item
                v-for="i in item.sliderItems"
                :key="`i${i.id}`"
                :item="i"
                class="col-md-6 col-xs-11"
              />
            </q-carousel-slide>
          </q-carousel>
        </q-tab-panel>
      </q-tab-panels>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, computed, Ref } from 'vue';
import { ITabPanel } from 'src/components/models';
import portfolioItem from './portfolio-item.vue';
//tab
let activeCarouselItem = ref('item1');
let tab = ref('All');
const tabs = ref([
  {
    id: 0,
    title: 'All',
  },
  {
    id: 1,
    title: 'Web',
  },
  {
    id: 2,
    title: 'Mobile',
  },
  {
    id: 3,
    title: 'UI/UX design',
  },
]);

const tabsPanels: Ref<ITabPanel[]> = ref([
  {
    id: 1,
    img: './images/portfolio2.png',
    imfo: '',
  },
  {
    id: 2,
    img: 'images/portfolio1.png',
    imfo: '',
  },
  {
    id: 3,
    img: 'images/portfolio2.png',
    imfo: '',
  },
  {
    id: 4,
    img: 'images/portfolio1.png',
    imfo: '',
  },
  {
    id: 5,
    img: 'images/portfolio2.png',
    imfo: '',
  },
  {
    id: 6,
    img: 'images/portfolio2.png',
    imfo: '',
  },
  {
    id: 7,
    img: 'images/portfolio1.png',
    imfo: '',
  },
  {
    id: 8,
    img: 'images/portfolio1.png',
    imfo: '',
  },
]);

function getCarouselItemInWidth(
  arr: ITabPanel[],
  n: number
): { name: string; sliderItems: ITabPanel[] }[] {
  let i = 0;
  let newArr: { name: string; sliderItems: ITabPanel[] }[] = [];
  while (arr.length != 0) {
    newArr.push({ name: `item${i + 1}`, sliderItems: arr.splice(0, n) });
    i++;
  }
  return newArr;
}

let count = computed(() => {
  if (screen.width <= 1024) {
    return 2;
  } else {
    return 4;
  }
});

let carouselItems = computed(() =>
  getCarouselItemInWidth(tabsPanels.value, count.value)
);
</script>

<style lang="scss" scoped>
@import '../../css/mixins.scss';
.portfolio {
  margin-bottom: $marginComponents;
  .activeTab {
    background: linear-gradient(140.44deg, #00002b 13.22%, #481186 96.97%);
    border-radius: 10px;
    color: white;
    font-family: 'Recursive', sans-serif !important;
  }
  .contentTab {
    color: #00002a;
    font-family: 'Recursive', sans-serif !important;
  }
  .slider-container {
    div {
      @include noteBook {
        padding: 0 0 2.6vw 2.6vw;
      }
    }
  }
}
</style>
