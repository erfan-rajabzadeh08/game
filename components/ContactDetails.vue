<template>
    <!-- Contact Details Start -->
    <div class="lg:mb-32 md:mb-20 mb-15">
        <div dir="rtl" class="container grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
            <div class="text-white align-center bg-no-repeat bg-scroll bg-center bg-cover md:pt-14 md:pb-12 md:px-12 sm:py-14 sm:px-6 py-14 px-10 h-460 pl-15" :style="{backgroundImage: `url(${ service.videoBannerBg })`}" v-for="(service, index) in services" :key="index">
                <div class="mb-120 align-center" :class="service.imageposition">
                    <img :src="service.imgSrc" :alt="service.name">
                </div>
                <div class="block" :class="service.contentposition">
                    <h3 class="text-white font-exo text-xl md:text-3xl font-bold uppercase mb-4">{{service.live}}</h3>
                    <span class="text-white">
                        <p class="text-lg leading-9">{{service.text}}</p>
                        <a :href="service.linkOnehref" class="block mb-2 last:mb-0 text-lg transition-all text-color " >{{service.linkOne}} </a>
                        <a :href="service.linkTwohref" class="block mb-2 last:mb-0 text-lg transition-all text-color ">{{service.linkTwo}}</a>
                    </span>
                </div>
            </div>
        </div>
    </div>
    <!-- Contact Details End -->
</template>

<script>
    export default {
        data() {
            return {
                services: [
                    {
                        imgSrc: "/images/icon/i.png",
                        name: "Service Image",
                        live: "اینستاگرام :",
                        videoBannerBg: "/images/others/gaming-world-bg3.webp",
                        imageposition: "text-right",
                        contentposition: "text-right",
                        linkOnehref: "https://www.instagram.com/club80.game?igsh=ZjRoM21vNTN2Zm5i",
                        linkOne: "گیم نت club80",
                      /*   linkTwohref: "mailto:support24@gmail.com",
                        linkTwo: "support24@gmail.com" */

                    },
                    {
                        imgSrc: "/images/icon/location.png",
                        name: "Service Image",
                        live: "آدرس :",
                        videoBannerBg: "/images/others/gaming-world-bg2.webp",
                        text: "کرمان رفسنجان خیابان اندیشه نبش کوچه17",
                        imageposition: "text-center",
                        contentposition: "text-center"
                    },
                    {
                        imgSrc: "/images/icon/phone.png",
                        name: "Service Image",
                        live: "شماره تماس :",
                        videoBannerBg: "/images/others/gaming-world-bg1.webp",
                        imageposition: "text-left",
                        contentposition: "text-right",
                        linkTwohref: "tel:09217913298",
                        linkTwo: "09217913298 ",

                       /*  linkTwohref: "+88(00)4568457437",
                        linkTwo: "+88 (00) 4568 457 437" */
                    }
                ]
            }
        },
    }
</script>
<style scoped>
.text-color:hover{
color:  rgb(79,95,255);
}
</style>