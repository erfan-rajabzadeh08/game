<template>
  <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg2.webp);">
    
    <HeaderSection/>

    <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
    
    <Breadcrumb :BreadcrumbTitle="BreadcrumbTitle" :BreadcrumbSubTitle="BreadcrumbSubTitle"/>

    <ContactDetails />

    <ContactForm />

    <GoogleMaps />

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
      ContactDetails: () => import('@/components/ContactDetails'),
      ContactForm: () => import('@/components/ContactForm'),
      GoogleMaps: () => import('@/components/GoogleMaps'),
      ContactBanner: () => import('@/components/ContactBanner'),
      Footer: () => import('@/components/Footer')
  },
  data() {
      return {
          navOpen: false,
          BreadcrumbTitle: "Contact Us",
          BreadcrumbSubTitle: "Contact-Us",
          paddingTop: "pt-32"
      }
  },
}
</script>