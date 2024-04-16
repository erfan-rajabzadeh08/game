<template>
    <!-- Hero Banner Start -->
    <div class="flex items-center relative bg-no-repeat bg-scroll bg-center bg-cover 2xl:h-940 xl:h-820 lg:h-780 md:h-650 sm:h-620 h-620 lg:mb-32 md:mb-20 mb-15" style="background-image:url(/images/bg/hero-bg1.webp);">
        <div class="container">
            <div class="relative 2xl:pt-20 lg:pt-16 md:pt-10 sm:pt-8 pt-8 md:mb-12 z-10 flex flex-col justify-center items-center lg:items-end lg:text-left text-center align-end">

                <h1 class="text-white text-right font-metal uppercase font-normal 2xl:text-7.5xl xl:text-8xl lg:text-5.5xl md:text-7xl text-5xl tracking-wide xl:mb-10 lg:mb-8 mb-5 text-shadow">بهترین بازی<br> بازی امروز است</h1>
                <p class="text-white font-semibold font-exo lg:mb-10 md:mb-6 text-base lg:text-3xl mb-5"> !فقط یک گیم نت نیست، یک سبک زندگی  <i>club80</i></p>

                <PrimaryButton/>

            </div>
        </div>
        <div class="absolute bottom-0 xl:left-14 lg:left-5 left-0 left-0 lg:left-auto text-center flex justify-center">
            <img class="2xl:w-940 xl:w-780 lg:w-650 md:w-620 w-450 md:text-center" src="/images/bg/hero-position-img.webp" alt="Position BG">
        </div>
    </div>
    <!-- Hero Banner End -->
</template>

<script>
    export default {
        components: {
            PrimaryButton: () => import('@/components/Button/PrimaryButton')
        }
    };
</script>