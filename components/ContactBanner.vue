<template>
    <!-- Contact Banner Section Start -->
    <div class="container" :class="paddingTop">
        <div class="flex justify-center md:justify-between flex-col md:flex-row items-center bg-no-repeat bg-scroll bg-center bg-cover lg:px-100 px-10 h-300" :style="{backgroundImage: `url(${ videoBannerBg })`}">
            <div>
                <h2 class="text-white md:text-4xl lg:text-5xl xl:text-title sm:text-3xl text-2xl text-center md:text-left mb-6 md:mb-0 uppercase font-bold leading-9 lg:leading-70">Connect with us <br> for gaming update.</h2>
            </div>
            <div>
                <n-link to="/contact" class="group primary-btn opacity-100 transition-all" style="background-image:url(/images/others/btn-bg.webp)">
                    {{btnName}}
                    <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                </n-link>
            </div>
        </div>
    </div>
    <!-- Contact Banner Section End -->
</template>

<script>
export default {
    props: {
        paddingTop: String,
    },
    data(){
        return {
            videoBannerBg: "/images/bg/gaming-update.webp",
            btnName: "Contact Now"
        }
    }
}
</script>