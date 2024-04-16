<template>
    <!-- Gaming World Section Start -->
    <div class="lg:mb-32 md:mb-20 mb-15">
        <div class="container">
            <TitleSection :title="title"/>
        </div>
        <div class="container grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
            <div class="text-white text-center align-cener bg-no-repeat bg-scroll bg-center bg-cover md:pt-14 md:pb-12 md:px-12 sm:py-14 sm:px-6 py-14 px-10 h-460" :style="{backgroundImage: `url(${ service.videoBannerBg })`}" v-for="(service, index) in services" :key="index">
                <div class="mb-12 text-center align-center">
                    <img class="h-37 w-36" :src="service.imgSrc" :alt="service.name">
                </div>
                <div class="block">
                    <h3 class="text-white font-exo text-xl md:text-2xl font-bold uppercase mb-4">{{service.live}}</h3>
                    <p class="">{{service.text}}</p>
                </div>
            </div>
        </div>
    </div>
    <!-- Gaming World Section End -->
</template>

<script>
    export default {
        components: {
            TitleSection: () => import('@/components/Title/TitleSection'),
        },
        data() {
            return {
                title:"You are most welcome In gaming world.",
                services: [
                    {
                        imgSrc: "/images/others/gaming-world1.webp",
                        name: "Service Image",
                        live: "Live Streaming",
                        text: "When unknown printer took type and scrambled it to make type specimen book centuries,",
                        videoBannerBg: "/images/others/gaming-world-bg1.webp"
                    },
                    {
                        imgSrc: "/images/others/gaming-world2.webp",
                        name: "Service Image",
                        live: "Game News",
                        text: "When unknown printer took type and scrambled it to make type specimen book centuries,",
                        videoBannerBg: "/images/others/gaming-world-bg2.webp"
                    },
                    {
                        imgSrc: "/images/others/gaming-world3.webp",
                        name: "Service Image",
                        live: "Game Tournaments",
                        text: "When unknown printer took type and scrambled it to make type specimen book centuries,",
                        videoBannerBg: "/images/others/gaming-world-bg3.webp"
                    },
                ]
            }
        },
    }
</script>