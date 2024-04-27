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
                title:"جدیدترین بازی ها، قوی ترین سیستم ها ",
                services: [
                    {
                        imgSrc: "/images/others/sport-image.png",
                        name: "Service Image",
                        live: "ورزشی ",
                        text: "در این ژانر محبوب، شما می توانید در نقش ورزشکاران محبوب خود ظاهر شوید و در قالب تیم های مورد علاقه تان به رقابت بپردازید",
                        videoBannerBg: "/images/others/gaming-world-bg1.webp"
                    },
                    {
                        imgSrc: "/images/others/gaming-world2.png",
                        name: "Service Image",
                        live: "اکشن ماجراجویی",
                        text: "آدرنالین در خون شما موج خواهد زد",
                        videoBannerBg: "/images/others/gaming-world-bg2.webp"
                    },
                    {
                        imgSrc: "/images/others/game3.png",
                        name: "Service Image",
                        live: "رازآلود معمایی       ",
                        text: "در اعماق تاریکی، جایی که سایه ها رازها را در آغوش خود می گیرند و سکوت فریاد می زند، آیا شجاعت کافی برای کشف حقیقت را دارید؟",
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
