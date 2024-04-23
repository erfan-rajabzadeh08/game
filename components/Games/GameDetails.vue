<template>
  <div class="container relative">
    <div class="relative overflow-hidden rounded-2xl">
          <img
            class="sm:h-full h-64 w-full object-cover"
            :src="games.gameImage"
          />
        </div>
    <!--         <p class="date text-primary font-bold mb-3 :">03 January, 2021, 05:01:00 AM</p>
 -->
    <!--  <h2 dir="rtl" class="  text-white font-bold uppercase xl:text-title lg:text-5xl md:text-4xl sm:text-3xl text-2xl xl:leading-70 lg:leading-12 leading-10 ">{{games.title}}</h2> -->
    <h3 dir="rtl" class="text-2xl text-white uppercase font-bold mt-16 ">
        توضیحات:
        </h3>
    <div class="content-details">
      <div class="description mt-5">
        <p class="leading-8"></p>
        <p dir="rtl" class="leading-8">{{ games.details }}</p>
      </div>

   <!--    <div class="gameslide my-15"> -->
        <!--             <swiper class="swiper" :options="swiperOption">
                    <swiper-slide v-for="(game, imageIndex) in gameslide" :key="imageIndex"> -->

        <!--     </swiper-slide>
                </swiper> -->

        <!-- Testimonial Arrows -->

        <!--            <div class="flex mt-10">
                    <div class="gameslide-button-prev swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all z-50 mr-2">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow2.webp" alt="">
                    </div>
                    <div class="gameslide-button-next swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape bg-cover transition-all z-50 ml-2">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow1.webp" alt="">
                    </div>
                </div>
             -->
   <!--    </div> -->

      <div dir="rtl" class=" description mt-6">
        <p class="leading-8">{{games.details1  }}</p>
        <p class="leading-8"> {{games.details2}} </p>
      </div>
      <section class="live-section mt-12">
      <div class="container relative">
        <CoolLightBox  :items="gameData" :index="index" :slider="false" @close="index = null ">
        </CoolLightBox>

        <swiper class="swiper" :options="swiperOption"   >
        <!--   <swiper-slide

          > -->
<div v-for="game in gameData"
            :key="game.slug">
            <div  v-if="game.slug===games.slug"  class="relative">
              <img
                class="sm:h-full h-64 w-full object-cover rounded-3xl"
                :src="`${game.gamingBg}`"
                :alt="game.gamingAlt"
              />
              <div @click="index = games.slug" class="absolute-center">
                <img
                  class="md:w-120 w-20 h-20 md:h-120 cursor-pointer rounded"
                  :src="`${game.playBtnOne}`"
                  :alt="game.playAlt"
                />
              </div>
              <div
                class="absolute md:h-20 h-12 left-1/2 bottom-0 transform -translate-x-2/4 bg-no-repeat bg-center w-full flex justify-center items-center"
                :style="{ backgroundImage: `url(${game.videoShapeBg})` }"
              >
                <h3
                  class="text-white font-exo font-bold uppercase text-base sm:text-xl md:text-2xl"
                >
                  {{ game.shapeTitle }}
                </h3>
              </div>
            </div>
        </div>
        <!--   </swiper-slide> -->
        </swiper>

        <!-- Testimonial Arrows -->

        <div
          class="livesection-button-prev swipper-arrow text-white absolute top-2/4 transform -translate-y-2/4 md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all 2xl:-left-28 left-3 z-50 cursor-pointer"
        >
          <img
            class="w-4 h-6"
            src="/images/icon/navigation-arrow2.webp"
            alt=""
          />
        </div>
        <div
          class="livesection-button-next swipper-arrow text-white absolute top-2/4 transform -translate-y-2/4 md:w-68 w-55 md:h-55 h-11 flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape bg-cover transition-all 2xl:-right-28 2xl:left-auto right-3 z-50 cursor-pointer"
        >
          <img
            class="w-4 h-6"
            src="/images/icon/navigation-arrow1.webp"
            alt=""
          />
        </div>
      </div>
    </section>





      <div class="description mt-6">
        <p class="leading-8">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500 when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap electro typesetting, remaining
          essentially unchanged. It was popularised in the 1960s with the
          release of Letraset sheets containing Lorem Ipsum passages, and more
          recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
        <p class="leading-8">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500 when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap electro typesetting, remaining
          essentially unchanged. It was popularised in the 1960s with the
          release of Letraset sheets containing Lorem Ipsum passages, and more
          recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
      </div>
      <div class="description mt-6">
        <h3 class="text-2xl text-primary uppercase font-bold mb-5">
          Whats New!
        </h3>
        <p class="leading-8">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500 when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap electro typesetting, remaining
          essentially unchanged. It was popularised in the 1960s with the
          release of Letraset sheets containing Lorem Ipsum passages, and more
          recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
      </div>

      <blockquote class="py-5 mb-5">
        <p class="font-bold text-yellow italic lg:text-3xl text-xl">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry has been the industry's standard dummy text ever since the
          1500 printer took galley of type scrambled it to make a type specimen
          book.
        </p>
      </blockquote>

      <div
        class="additional-information-area bg-secondary-100 px-9 py-9 rounded-2xl mb-9"
      >
        <h3 class="text-2xl text-white uppercase font-bold mb-6">
          Additional Information:
        </h3>
        <div
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-5 gap-5 text-white"
        >
          <div class="additional_information_text">
            <h4 class="font-bold mb-5">Updated:</h4>
            <p class="text-gray-400">2021-01-02</p>
          </div>
          <div class="additional_information_text">
            <h4 class="font-bold mb-5">SIZE:</h4>
            <p class="text-gray-400">98MB</p>
          </div>
          <div class="additional_information_text">
            <h4 class="font-bold mb-5">INSTALLS:</h4>
            <p class="text-gray-400">80,000,000+</p>
          </div>
          <div class="additional_information_text">
            <h4 class="font-bold mb-5">CURRENT VERSION:</h4>
            <p class="text-gray-400">03.00.28.00.00</p>
          </div>
          <div class="additional_information_text">
            <h4 class="font-bold mb-5">IN-APP PRODUCTS:</h4>
            <p class="text-gray-400">$0.85 - $985.00</p>
          </div>
        </div>
      </div>
      <div class="description mt-6">
        <p class="leading-8">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500 when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap electro typesetting, remaining
          essentially unchanged. It was popularised in the 1960s with the
          release of Letraset sheets containing Lorem Ipsum passages, and more
          recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
        <p class="leading-8">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500 when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap electro typesetting, remaining
          essentially unchanged. It was popularised in the 1960s with the
          release of Letraset sheets containing Lorem Ipsum passages, and more
          recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
      </div>
    </div>

    <Disqus class="mt-10" shortname="Admin" />


  </div>
</template>

<script>
import CoolLightBox from "vue-cool-lightbox";
import "vue-cool-lightbox/dist/vue-cool-lightbox.min.css";
import gameData from "@/data/games.json";
import "@/assets/css/swiper.css";
import { Swiper } from "vue-awesome-swiper";
import { Disqus } from "vue-disqus";
export default {
  components: {
    Swiper,
    Disqus,
    CoolLightBox,
  },
  props: ["games"],
  data() {
    return {
      gameData,

        swiperOption: {
          slidesPerView: 1,
          spaceBetween: 30,
          pagination: false,
          navigation: {
            nextEl: '.live-section .livesection-button-next',
            prevEl: '.live-section .livesection-button-prev'
          }
        },

      index: null,
      slideshow:false,
      loop:false,
      zIndex:10000000,
      gameslide: [
        {
          gamingBg: "/images/others/game-details-thumb.webp",
        },
        /*  {
                    gamingBg: "/images/others/game-details-thumb.webp"
                },
                {
                    gamingBg: "/images/others/game-details-thumb.webp"
                } */
      ],
    };
  },
};
</script>
