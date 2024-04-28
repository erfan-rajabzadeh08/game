<template>
    <!-- Hero Banner Start -->
    <div class="flex items-center relative bg-no-repeat bg-scroll bg-center bg-cover 2xl:h-940 xl:h-820 lg:h-780 md:h-650 sm:h-620 h-620 lg:mb-32 md:mb-20 mb-15" style="background-image:url(/images/bg/hero-bg1.webp);">
        <div class="container">
            <div class="relative 2xl:pt-20 lg:pt-16 md:pt-10 sm:pt-8 pt-8 md:mb-12 z-10 flex flex-col justify-center items-center lg:items-end lg:text-left text-center align-end">

                <h1 class="h1-fontsize text-white text-right font-metal uppercase font-normal  2xl:text-7xl xl:text-7xl lg:text-6xl md:text-6xl text-4xl tracking-wide xl:mb-10 lg:mb-8 mb-5 text-shadow">اینجا فقط بازی نیست<br> سرزمین عجایب 80 است</h1>
                <p class="text-white font-semibold font-exo lg:mb-10 md:mb-6 text-base lg:text-3xl mb-5">!جایی که بازی، زندگی می شود<i>club80</i></p>

                <PrimaryButton/>

            </div>
        </div>
        <div class="absolute bottom-0 xl:left-14 lg:left-5 left-0 left-0 lg:left-auto text-center flex justify-center">
            <img class=" shake-vertical 2xl:w-940 xl:w-780 2xl:h-940 lg:h-780 lg:w-650 md:w-620 w-500  md:text-center" src="/images/bg/test.png" alt="Position BG">
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

<style scoped>

.shake-vertical {
	-webkit-animation: shake-vertical 30s cubic-bezier(0.455, 0.030, 0.515, 0.955) infinite reverse backwards;
	        animation: shake-vertical 30s cubic-bezier(0.455, 0.030, 0.515, 0.955) infinite reverse backwards;
}


 @-webkit-keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
  }
  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-8px);
            transform: translateY(-8px);
  }
  20%,
  40%,
  60% {
    -webkit-transform: translateY(8px);
            transform: translateY(8px);
  }
  80% {
    -webkit-transform: translateY(6.4px);
            transform: translateY(6.4px);
  }
  90% {
    -webkit-transform: translateY(-6.4px);
            transform: translateY(-6.4px);
  }
}
@keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
  }
  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-8px);
            transform: translateY(-8px);
  }
  20%,
  40%,
  60% {
    -webkit-transform: translateY(8px);
            transform: translateY(8px);
  }
  80% {
    -webkit-transform: translateY(6.4px);
            transform: translateY(6.4px);
  }
  90% {
    -webkit-transform: translateY(-6.4px);
            transform: translateY(-6.4px);
  }
}

 @media only screen and (min-width: 1000px) {
.h1-fontsize{
  line-height: 1.2 !important ;
}
}
@media only screen and (max-width: 1000px) {
    .shake-vertical{
    opacity: 0.5;
}
.h1-fontsize{
  line-height: 1.5 !important ;
}
}

</style>