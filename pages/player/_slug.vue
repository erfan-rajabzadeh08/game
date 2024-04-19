<template>
    <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">

        <HeaderSection/>

        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

        <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

        <div class="container">
            <div class="flex md:flex-row flex-col bg-secondary-100 p-8 md:p-68 rounded-50">
                <div class="md:w-2/5">

                    <div class="border-4 border-gray-400 rounded-3xl d-flex max-w-full md:max-w-sm overflow-hidden">
                        <img class="w-full" :src="playerData.imgSrc" alt="">
                    </div>

                    <div class="flex flex-col justify-center items-center relative mt-8 max-w-full md:max-w-sm z-10 py-7">
                        <h3 class="text-white font-bold text-lg md:text-2xl uppercase">
                            <n-link :to="`/player/${playerData.slug}`">{{playerData.name}}</n-link>
                        </h3>
                        <span class="text-white text-sm md:text-base transition-all">{{playerData.subtitle}}</span>
                        <div class="absolute top-0 left-0 w-full z-n1">
                            <img class="absolute w-full h-120" src="/images/others/tam-text-shape2.webp" alt="">
                        </div>
                    </div>

                    <ul class="flex justify-center text-white mt-8 max-w-full md:max-w-sm">
                        <li class="mr-2">
                            <a href="https://www.twitch.tv" class="w-12 h-12 rounded-full border-2 border-yellow flex justify-center items-center hover:border-yellow hover:bg-yellow transition-all"><i class="icofont-twitch"></i></a>
                        </li>
                        <li class="mr-2 ml-2">
                            <a href="https://www.youtube.com" class="w-12 h-12 rounded-full border-2 border-bright flex justify-center items-center hover:border-bright hover:bg-bright transition-all"><i class="icofont-youtube-play"></i></a>
                        </li>
                        <li class="ml-2">
                            <a href="https://www.twitter.com" class="w-12 h-12 rounded-full border-2 border-punch flex justify-center items-center hover:border-punch hover:bg-punch transition-all"><i class="icofont-twitter"></i></a>
                        </li>
                    </ul>

                </div>
                <div class="md:w-3/5 md:pl-10 mt-16 md:mt-0">

                    <div class="about_title lg:mb-6 mb-4">
                        <h5 class="text-primary text-xl uppercase font-bold pl-24 lg:mb-6 mb-4 relative before:absolute content-before before:left-0 before:top-1/2 before:-translate-y-1/2 before:transform before:h-1 before:bg-primary before:w-16">Player Profile</h5>
                        <h2 class="text-white font-exo font-bold uppercase xl:text-title lg:text-5xl md:text-4xl sm:text-3xl text-2xl xl:leading-70 lg:leading-12 leading-10 max-w-sm md:max-w-xl lg:max-w-2xl"> {{playerData.title}} </h2>
                    </div>

                    <div class="about_desc mb-10">
                        <p class="lg:text-xl lg:leading-8">It is a long established fact that a reader will be distracted the readable content of page when looking at it layout the point using lorem Ipsum is that it has a more-or-less normal distribution.</p>
                        <p class="lg:text-xl lg:leading-8">It is a long established fact that a reader will be distracted the readable content of page when looking at it layout the point using lorem Ipsum is that it has a more-or-less normal distribution.</p>
                    </div>

                    <div class="about_btn">
                        <n-link to="/contact" class="group primary-btn opacity-100 transition-all" style="background-image:url(/images/others/btn-bg.webp)">Contact Now <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all"></n-link>  
                    </div>
                    
                </div>
            </div>
        </div>

        <CounterUp/>

        <ContactBanner :paddingTop="paddingTop"/>

        <Footer/>

    </div>
</template>

<script>

    import playerData from '@/data/player.json'
    export default {
        components: {
            HeaderSection: () => import('@/components/HeaderSection'),
            OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
            Breadcrumb: () => import('@/components/Breadcrumb'),
            CounterUp: () => import('@/components/CounterUp'),
            ContactBanner: () => import('@/components/ContactBanner'),
            Footer: () => import('@/components/Footer')
        },
        data() {
            return {
                playerData,
                navOpen: false,
                BreadcrumbTitle: "Player Details",
                BreadcrumbSubTitle: "Player",
                paddingTop: "pt-0",
                slug: this.$route.params.slug
            };
        },
        mounted () {
            this.playerData = playerData.find(player => player.slug == this.$route.params.slug);
        }
    }

</script>