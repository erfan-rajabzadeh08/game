<template>
  <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">
    
    <HeaderSection/>

    <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
    
    <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

    <AboutUs/>

    <CounterUp/>

    <LiveStream/>

    <GamerTeam/>

    <Testimonial/>

    <ContactBanner :paddingTop="paddingTop"/>

    <Footer/>

  </div>
</template>

<script>
export default {
  components: {
      HeaderSection: () => import('@/components/HeaderSection'),
      OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
      Breadcrumb: () => import('@/components/Breadcrumb'),
      AboutUs: () => import('@/components/AboutUs'),
      CounterUp: () => import('@/components/CounterUp'),
      LiveStream: () => import('@/components/LiveStream'),
      GamerTeam: () => import('@/components/GamerTeam'),
      Testimonial: () => import('@/components/Testimonial'),
      ContactBanner: () => import('@/components/ContactBanner'),
      Footer: () => import('@/components/Footer')
  },
  data() {
      return {
          navOpen: false,
          BreadcrumbTitle: "About Us",
          BreadcrumbSubTitle: "About Us",
          paddingTop: "pt-32"
      }
  },
}
</script>