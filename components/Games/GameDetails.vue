<template>
    <div class="container relative">
        <p class="date text-primary font-bold mb-3">03 January, 2021, 05:01:00 AM</p>
        <h2 class="text-white font-bold uppercase xl:text-title lg:text-5xl md:text-4xl sm:text-3xl text-2xl xl:leading-70 lg:leading-12 leading-10">{{games.title}}</h2>
        <div class="content-details">
            <div class="description mt-6">
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>

            <div class="gameslide my-15">

                <swiper class="swiper" :options="swiperOption">
                    <swiper-slide v-for="(game, imageIndex) in gameslide" :key="imageIndex">
                        <div class="relative">
                            <img class="sm:h-full h-64 w-full object-cover" :src="`${game.gamingBg}`">
                        </div>
                    </swiper-slide>
                </swiper>

                <!-- Testimonial Arrows -->

                <div class="flex mt-10">
                    <div class="gameslide-button-prev swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all z-50 mr-2">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow2.webp" alt="">
                    </div>
                    <div class="gameslide-button-next swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape bg-cover transition-all z-50 ml-2">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow1.webp" alt="">
                    </div>
                </div>
            </div>

            <div class="description mt-6">
                <h3 class="text-2xl text-white uppercase font-bold mb-5">Description:</h3>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
            <div class="description mt-6">
                <h3 class="text-2xl text-white uppercase font-bold mb-5">Features:</h3>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
            <div class="description mt-6">
                <h3 class="text-2xl text-primary uppercase font-bold mb-5">Whats New!</h3>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>

            <blockquote class="py-5 mb-5">
                <p class="font-bold text-yellow italic lg:text-3xl text-xl">Lorem Ipsum is simply dummy text of the printing and typesetting industry has been the industry's standard dummy text ever since the 1500 printer took galley of type scrambled it to make a type specimen book.</p>
            </blockquote>

            <div class="additional-information-area bg-secondary-100 px-9 py-9 rounded-2xl mb-9">
                <h3 class="text-2xl text-white uppercase font-bold mb-6">Additional Information:</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-5 gap-5 text-white">
                    <div class="additional_information_text">
                        <h4 class="font-bold mb-5">Updated:</h4>
                        <p class=" text-gray-400">2021-01-02</p>
                    </div>
                    <div class="additional_information_text">
                        <h4 class="font-bold mb-5">SIZE:</h4>
                        <p class=" text-gray-400">98MB</p>
                    </div>
                    <div class="additional_information_text">
                        <h4 class="font-bold mb-5">INSTALLS:</h4>
                        <p class=" text-gray-400">80,000,000+</p>
                    </div>
                    <div class="additional_information_text">
                        <h4 class="font-bold mb-5">CURRENT VERSION:</h4>
                        <p class=" text-gray-400">03.00.28.00.00</p>
                    </div>
                    <div class="additional_information_text">
                        <h4 class="font-bold mb-5">IN-APP PRODUCTS:</h4>
                        <p class=" text-gray-400">$0.85 - $985.00</p>
                    </div>
                </div>
            </div>
            <div class="description mt-6">
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                <p class="leading-8">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap electro typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
        </div>
        
        <Disqus class=" mt-10" shortname='Admin' />
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
import { Disqus } from 'vue-disqus'
export default {
    components: {
        Swiper,
        SwiperSlide,
        Disqus
    },
    props: ["games"],
    data () {
        return {    
            swiperOption: {
                slidesPerView: 1,
                spaceBetween: 30,
                pagination: false,
                navigation: {
                    nextEl: '.gameslide .gameslide-button-next',
                    prevEl: '.gameslide .gameslide-button-prev'
                }
            },
            gameslide: [
                {
                    gamingBg: "/images/others/game-details-thumb.webp"
                },
                {
                    gamingBg: "/images/others/game-details-thumb.webp"
                },
                {
                    gamingBg: "/images/others/game-details-thumb.webp"
                }
            ]
        }
    }
}
</script>