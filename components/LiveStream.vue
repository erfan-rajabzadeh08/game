<template>
  <!-- Live Section Start -->
  <section class="live-section">
    <div class="container relative">

      <CoolLightBox
        :items="matchesData"
        :index="index"
        @close="index = null">
      </CoolLightBox>

      <swiper class="swiper" :options="swiperOption">
        <swiper-slide v-for="(match, imageIndex) in matchesData" :key="imageIndex">
          <div class="relative">
            <img class="sm:h-full h-64 w-full object-cover" :src="`${match.gamingBg}`" :alt="match.gamingAlt">
            <div @click="index = imageIndex" class="absolute-center">
              <img class="md:w-120 w-20 h-20 md:h-120 cursor-pointer rounded" :src="`${match.playBtnOne}`" :alt="match.playAlt">
            </div>
            <div class="absolute md:h-20 h-12 left-1/2 bottom-0 transform -translate-x-2/4 bg-no-repeat bg-center w-full flex justify-center items-center" :style="{backgroundImage: `url(${ match.videoShapeBg })`}">
              <h3 class="text-white font-exo font-bold uppercase text-base sm:text-xl md:text-2xl">{{ match.shapeTitle }}</h3>
            </div>
          </div>
        </swiper-slide>
      </swiper>

      <!-- Testimonial Arrows -->

      <div class="livesection-button-prev swipper-arrow text-white absolute top-2/4 transform -translate-y-2/4 md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all 2xl:-left-28 left-3 z-50 cursor-pointer">
        <img class="w-4 h-6" src="/images/icon/navigation-arrow2.webp" alt="">
      </div>
      <div class="livesection-button-next swipper-arrow text-white absolute top-2/4 transform -translate-y-2/4 md:w-68 w-55 md:h-55 h-11 flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape bg-cover transition-all 2xl:-right-28 2xl:left-auto right-3 z-50 cursor-pointer">
        <img class="w-4 h-6" src="/images/icon/navigation-arrow1.webp" alt="">
      </div>
    </div>
  </section>
  <!-- Live Section End -->
</template>

<script>
  import CoolLightBox from 'vue-cool-lightbox'
  import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css'
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
  import '../assets/css/swiper.css';
  import matchesData from '../data/matches.json'
  
  export default {

    components: {
      Swiper,
      SwiperSlide,
      CoolLightBox
    },
    data() {
      return {
        matchesData,
        swiperOption: {
          slidesPerView: 1,
          spaceBetween: 30,
          pagination: false,
          navigation: {
            nextEl: '.live-section .livesection-button-next',
            prevEl: '.live-section .livesection-button-prev'
          }
        },
        index: null
      }
    }
  }
</script>