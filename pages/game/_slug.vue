<template>
    <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">

        <HeaderSection/>

        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

        <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

        <GameDetails :games="gameHome"/>

        <ContactBanner :paddingTop="paddingTop"/>

        <Footer/>

    </div>
</template>

<script>

    import gameHome from '@/data/games.json'
    export default {
        components: {
            GameDetails: () => import('@/components/Games/GameDetails'),
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
                gameHome,
                navOpen: false,
                BreadcrumbTitle: "Game Details",
                BreadcrumbSubTitle: "Game",
                paddingTop: "pt-32",
                slug: this.$route.params.slug
            };
        },
        mounted () {
            this.gameHome = gameHome.find(games => games.slug == this.$route.params.slug);
        }
    }

</script>