<template>
  <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">
    
    <HeaderSection/>

    <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
    
    <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

    <section class="container">
        <div class="grid gap-8 sm:grid-cols-2 md:grid-cols-3">
            <div class="single_blog items-center" v-for="(blog, index) in blogData" :key="index">
                <div class="blog_thumb">
                    <n-link :to="`/blog/${blog.slug}`">
                        <img class="rounded-xl" :src="blog.blogGrid" :alt="blog.alt">
                    </n-link>
                </div>
                <div class="blog_content mt-6">
                    <span class="text-sm text-white font-exo font-normal mb-2 sm:mb-5 block"><i class="icofont-calendar text-primary mr-2"></i>{{blog.date}}</span>
                    <h2 class="text-white xl:text-2xl lg:text-xl md:text-2xl sm:text-lg text-lg font-bold uppercase font-exo hover:text-primary transition-all mb-2 sm:mb-5 leading-9">
                        <n-link :to="`/blog/${blog.slug}`">{{blog.title}}</n-link>
                    </h2>
                    <n-link :to="`/blog/${blog.slug}`" class="uppercase font-exo relative pl-12 text-sm text-white transition-all hover:text-primary before:empty-content before:absolute before:h-0.5 before:w-7.5 before:bg-primary before:left-0 before:top-1/2 before:transform before:-translate-y-1/2">Read More</n-link>
                </div>
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