<template>
    <!-- Gaming World Section Start -->
    <div class="lg:mb-32 md:mb-20 mb-15">
        <div class="container">
            <TitleSection :title="title"/>
        </div>
        <div class="container grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
            <div class="text-white text-center align-cener bg-no-repeat bg-scroll bg-center bg-cover md:pt-14 md:pb-12 md:px-12 sm:py-14 sm:px-6 py-14 px-10 h-460" :style="{backgroundImage: `url(${ service.videoBannerBg })`}" v-for="(service, index) in services" :key="index">
                <div class="mb-12 text-center align-center">
                    <img class=" image-sport" :src="service.imgSrc" :alt="service.name">
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
                title:"بهترین و پر هیجان ترین سبک بازی های دنیا",
                services: [
                    {
                        imgSrc: "/images/others/sport-image.png",
                        name: "Service Image",
                        live: "ورزشی ",
                        text: "هیجانات و در کنار تمزکز را توی زمین فوتبال می توان تجربه کرد ",
                        videoBannerBg: "/images/others/gaming-world-bg1.webp"
                    },
                    {
                        imgSrc: "/images/others/gaming-world2.png",
                        name: "Service Image",
                        live: "اکشن",
                        text: "ساعتی رو فقط با حریفت مبارزه کن و استراتژی های خودتو نشون بده",
                        videoBannerBg: "/images/others/gaming-world-bg2.webp"
                    },
                    {
                        imgSrc: "/images/others/game3.png",
                        name: "Service Image",
                        live: "معمایی و راز آلود",
                        text: "اگردنبال بازی های پیچیده و مفهومی هستی میتونی ساعت ها بشینی از این بازی ها لذت ببری",
                        videoBannerBg: "/images/others/gaming-world-bg3.webp"
                    },
                ]
            }
        },
    }
</script>

<style scoped>
.image-sport{
    width: 11.875rem;
    height: 11.25rem;
}
</style>
