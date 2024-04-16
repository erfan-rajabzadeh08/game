<template>
  <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">
    
    <HeaderSection/>

    <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
    
    <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

    <section class="container">
        <div class="grid md:gap-6 lg:gap-8 grid-cols-1 md:grid-cols-12">
            <div class="md:col-span-7 lg:col-span-8 row-start-1 md:row-auto">
                <BlogGrid />
            </div>
            <div class="md:col-span-5 lg:col-span-4 row-start-2 md:row-auto">
                <BlogSidebar />
            </div>
        </div>
    </section>

    <ContactBanner :paddingTop="paddingTop"/>

    <Footer/>

  </div>
</template>

<script>
import blogData from '@/data/blog.json'
export default {
    components: {
        HeaderSection: () => import('@/components/HeaderSection'),
        OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
        Breadcrumb: () => import('@/components/Breadcrumb'),
        ContactBanner: () => import('@/components/ContactBanner'),
        Footer: () => import('@/components/Footer')
    },
    data() {
        return {
            blogData,
            navOpen: false,
            BreadcrumbTitle: "Blog Without Sidebar",
            BreadcrumbSubTitle: "Blog without sidebar",
            paddingTop: "pt-32"
        }
    },
}
</script>