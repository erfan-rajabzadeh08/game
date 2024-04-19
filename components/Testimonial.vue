<template>
    <!-- Testimonial Section Start -->
    <section class="testimonial-section">
        <div class="relative pt-120 pb-120 before:empty-content before:absolute before:invisible sm:before:visible before:right-0 lg:before:h-3 before:h-2 before:w-1/3 before:bg-primary before:top-40 lg:before:top-48" style="background-image:url(/images/others/testimonial-bg-fullwidth.webp)">

            <div class="container relative">
                <h2 class="font-exo mb-15 text-white text-3xl sm:text-4xl lg:text-title font-bold uppercase leading-8 sm:leading-10 lg:leading-70 text-center sm:text-left">What people’s say <br> ABOUT <span class="text-primary">game studio. </span></h2>

                <swiper class="swiper" :options="swiperOption">
                    <swiper-slide v-for="(testimonial, index) in testimonialData" :key="index">
                        <div class="flex flex-col md:flex-row lg:flex-row xl:flex-row 2xl:flex-row items-center bg-cover py-10 px-8 md:py-55 md:px-16 lg:py-73 lg:px-24 rounded-50" style="background-image:url(/images/others/testimonial-bg.webp)">
                            <div class="w-28 sm:w-230 lg:w-260 flex-shrink-0">
                                <img :src="testimonial.clientImage" alt="Testimonial">
                            </div>
                            <div class="flex-grow text-center md:text-left lg:text-left xl:text-left 2xl:text-left mt-8 md:mt-0 md:ml-14">
                                <p class="text-base lg:text-xl lg:leading-9 leading-loose">
                                    {{testimonial.description}}
                                </p>
                                <div class="mt-5">
                                    <h3 class="font-bold uppercase text-white text-2xl">{{testimonial.name}}</h3>
                                    <span class="text-primary mt-5 block">{{testimonial.designation}}</span>
                                </div>
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>

                <!-- Testimonial Arrows -->
                <div class="flex justify-center mt-14">
                    <div class="testimonial-button-prev swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all mr-4 cursor-pointer">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow2.webp" alt="Arrow">
                    </div>
                    <div class="testimonial-button-next swipper-arrow text-white md:w-68 w-55 md:h-55 h-11 bg-cover flex items-center justify-center hover:bg-arrow-hover-shape bg-arrow-shape transition-all ml-4 cursor-pointer">
                        <img class="w-4 h-6" src="/images/icon/navigation-arrow1.webp" alt="Arrow">
                    </div>
                </div>

            </div>

        </div>
    </section>
    <!-- Testimonial Section End -->
</template>

<script>
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
    import testimonialData from '../data/testimonial.json'
    
    export default {

        components: {
            Swiper,
            SwiperSlide
        },
        data() {
            return {
                testimonialData,
                swiperOption: {
                    slidesPerView: 1,
                    spaceBetween: 30,
                    pagination: false,
                    navigation: {
                        nextEl: '.testimonial-section .testimonial-button-next',
                        prevEl: '.testimonial-section .testimonial-button-prev'
                    }
                }
            }
        }
    }
</script>