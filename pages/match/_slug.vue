<template>
    <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">

        <HeaderSection/>

        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

        <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

        <!-- Team Varses Team Start -->
        <div class="container mb-12">
            <div class="border-4 border-light-blue-500 rounded-4xl px-10 lg:px-16 py-8 max-w-lg mx-auto">
                <div class="grid grid-cols-1 items-center">
                    <div class="flex justify-center items-center w-full px-20 sm:px-0">
                        <img class="lg:mr-9 mr-5" :src="matchesData.teamOne" alt="Feature Icon">
                        <img class="lg:mr-9 mr-5" :src="matchesData.teamVs" alt="Feature Icon">
                        <img :src="matchesData.teamTwo" alt="Feature Icon">
                    </div>
                </div>
            </div>
        </div>
        <!-- Team Varses Team End -->

        <!-- Game Live Streaming Start -->
        <div class="container relative">
            <img class="sm:h-full h-64 w-full object-cover" :src="`${matchesData.gamingBg}`" :alt="matchesData.gamingAlt">
            <div @click="$modal.show('my-modal')" class="absolute-center">
                <img class="md:w-120 w-20 h-20 md:h-120 cursor-pointer rounded" :src="`${matchesData.playBtnOne}`" :alt="matchesData.playAlt">
            </div>
            <client-only>
                <modal class="bg-transparent" name="my-modal" :width="1000" :height="700" :adaptive="true">
                    <div class="modal-content w-full h-full">
                        <iframe class="w-full h-full" :src="`${matchesData.src}`" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                        <button class="absolute top-0 right-0 icofont-close-line z-999 font-bold text-3xl text-black hover:text-primary transition-all transform hover:rotate-90" @click="$modal.hide('my-modal')"></button>
                    </div>
                </modal>
            </client-only>
            <div class="absolute md:h-20 h-12 left-1/2 bottom-0 transform -translate-x-2/4 bg-no-repeat bg-center w-full flex justify-center items-center" :style="{backgroundImage: `url(${ matchesData.videoShapeBg })`}">
                <h3 class="text-white font-exo font-bold uppercase text-base sm:text-xl md:text-2xl">{{ matchesData.shapeTitle }}</h3>
            </div>
        </div>
        <!-- Game Live Streaming End -->

        <!-- Match Counterup Start -->
        <div class="container">
            <div class="match_details_counterup flex flex-col sm:flex-row justify-between items-center py-12 mb-12 border-b-2 border-secondary-80">
                <div v-observe-visibility="{callback: visibilityChanged, once: true}">
                    <div v-if="commentsVisible" class="grid grid-cols-3">
                        <div class="mr-6 pr-6 lg:mr-16 lg:pr-16 relative pt-4">
                            <p class="uppercase md:text-lg text-sm font-semibold text-primary">Player:</p>
                            <countTo class="text-white text-4xl lg:text-5xl font-bold" :startVal='0' :endVal='280' :duration='3000' :autoplay='true'></countTo>
                            <span class="absolute right-0 top-0 transform rotate-12 bg-secondary-80 h-28 w-0.5"></span>
                        </div>
                        <div class=" mr-6 pr-6 lg:mr-20 lg:pr-20 relative pt-4">
                            <p class="uppercase md:text-lg text-sm font-semibold text-primary">Team:</p>
                            <countTo class="text-white text-4xl lg:text-5xl font-bold" :startVal='0' :endVal='16' :duration='3000' :autoplay='true'></countTo>
                            <span class="absolute right-0 top-0 transform rotate-12 bg-secondary-80 h-28 w-0.5"></span>
                        </div>
                        <div class=" mr-6 pr-6 lg:mr-16 lg:pr-16 relative pt-4">
                            <p class="uppercase md:text-lg text-sm font-semibold text-primary">Winning Prize:</p>
                            <countTo class="text-white text-4xl lg:text-5xl font-bold" :startVal='0' :endVal='6800' :duration='3000' :autoplay='true'></countTo>
                        </div>
                    </div>
                </div>
                <div class="flex justify-end mt-16 md:mt-0">
                    <n-link to="/contact" class="group primary-btn opacity-100 transition-all" style="background-image:url(/images/others/btn-bg.webp)">
                        {{btnName}}
                        <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                    </n-link>  
                </div>
            </div>
        </div>
        <!-- Match Counterup End -->

        <MatchDetails :match="matchesData"/>

        <ContactBanner :paddingTop="paddingTop"/>

        <Footer/>

    </div>
</template>

<script>

    import countTo from 'vue-count-to';
    import { Swiper, SwiperSlide } from 'vue-awesome-swiper';
    import matchesData from '@/data/matches.json'
    export default {
        components: {
            Swiper,
            SwiperSlide,
            countTo,
            MatchDetails: () => import('@/components/Matches/MatchDetails'),
            HeaderSection: () => import('@/components/HeaderSection'),
            OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
            Breadcrumb: () => import('@/components/Breadcrumb'),
            CounterUp: () => import('@/components/CounterUp'),
            ContactBanner: () => import('@/components/ContactBanner'),
            Footer: () => import('@/components/Footer')
        },
        data() {
            return {
                btnName: "JOIN NOW",
                commentsVisible: false,
                swiperOption: {
                    slidesPerView: 1,
                    spaceBetween: 30,
                    pagination: false,
                    navigation: {
                        nextEl: '.live-section .livesection-button-next',
                        prevEl: '.live-section .livesection-button-prev'
                    }
                },
                matchesData,
                navOpen: false,
                BreadcrumbTitle: "Match Details",
                BreadcrumbSubTitle: "Match",
                paddingTop: "pt-32",
                slug: this.$route.params.slug
            };
        },
        mounted () {
            this.matchesData = matchesData.find(match => match.slug == this.$route.params.slug);
        },
        methods: {
            visibilityChanged(isVisible) {
                this.commentsVisible = isVisible;
            },
        }
    }

</script>