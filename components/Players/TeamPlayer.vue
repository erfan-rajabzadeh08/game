<template>
    <!-- Team Number Section Start -->
    <div class="my-16">
        <div class="team-one">
            <span class="text-primary text-lg uppercase font-semibold mb-4 block">Team - 01</span>
            <h2 class="font-bold uppercase text-xl md:text-4xl mb-8">Fanda’S players</h2>
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide v-for="(team, index) in teamplayers" :key="index">
                    <div class="rounded-50">
                        <div class="">
                            <img :src="team.teamImage" alt="Team Image">
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
        <div class="team-one mt-16">
            <span class="text-primary text-lg uppercase font-semibold mb-4 block">Team - 02</span>
            <h2 class="font-bold uppercase text-xl md:text-4xl mb-8">Ninja’S players</h2>
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide v-for="(team, index) in teamplayers.slice(2, 9)" :key="index">
                    <div class="rounded-50">
                        <div class="">
                            <img :src="team.teamImage" alt="Team Image">
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
    <!-- Team Number Section End -->
</template>

<script>
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
    export default {

        components: {
            Swiper,
            SwiperSlide
        },
        data() {
        return {
                swiperOption: {
                    slidesPerView: 6,
                    spaceBetween: 30,
                    loop: true,
                    pagination: false,
                    navigation: false,
                    breakpoints: {
                        // when window width is >= 320px
                        320: {
                        slidesPerView: 2,
                        spaceBetween: 20
                        },
                        // when window width is >= 480px
                        480: {
                        slidesPerView: 3,
                        spaceBetween: 30
                        },
                        // when window width is >= 640px
                        768: {
                        slidesPerView: 4,
                        spaceBetween: 40
                        },
                        // when window width is >= 1024px
                        1024: {
                        slidesPerView: 6,
                        spaceBetween: 40
                        }
                    },
                },
                teamplayers: [
                    {
                        teamImage: "/images/others/players1.webp"
                    },
                    {
                        teamImage: "/images/others/players2.webp"
                    },
                    {
                        teamImage: "/images/others/players3.webp"
                    },
                    {
                        teamImage: "/images/others/players4.webp"
                    },
                    {
                        teamImage: "/images/others/players5.webp"
                    },
                    {
                        teamImage: "/images/others/players6.webp"
                    },
                    {
                        teamImage: "/images/others/players3.webp"
                    },
                    {
                        teamImage: "/images/others/players1.webp"
                    },
                    {
                        teamImage: "/images/others/players2.webp"
                    },
                ]
            }
        }
    }

</script>
