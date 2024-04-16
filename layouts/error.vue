<template>
    <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">

        <HeaderSection/>

        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

        <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

        <NuxtError/>

        <Footer/>

    </div>
</template>

<script>
export default {
    components: {
        HeaderSection: () => import('@/components/HeaderSection'),
        OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
        Breadcrumb: () => import('@/components/Breadcrumb'),
        NuxtError: () => import('@/components/NuxtError'),
        ContactBanner: () => import('@/components/ContactBanner'),
        Footer: () => import('@/components/Footer'),
    },
    data() {
        return {
            navOpen: false,
            BreadcrumbTitle: "Error Page",
            BreadcrumbSubTitle: "Pages"
        }
    },
}
</script>