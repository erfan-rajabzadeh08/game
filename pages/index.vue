<template>
  <div class="bg-cover bg-gray-800" style="background-image:url(/images/bg/body-bg.webp);">

    <HeaderSection/>

    <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

    <HeroBanner/>

    <GamingWorld/>

    <LiveStream/>

<<<<<<< HEAD
<!--     <UpcomingMatchesHome/> -->

   <!--  <CounterUp/> -->

    <PopularGame/>

<!--     <Testimonial/> -->

<!--     <BlogPost/> -->
=======
    <UpcomingMatchesHome/>

    <CounterUp/>

    <PopularGame/>

    <Testimonial/>

    <BlogPost/>
>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b

    <ContactBanner :paddingTop="paddingTop"/>

    <Footer/>

  </div>
</template>

<script>
export default {
  components: {
      HeaderSection: () => import('@/components/HeaderSection'),
      HeroBanner: () => import('@/components/HeroBanner'),
      OffCanvasMobileMenu: () => import('@/components/Header/OffCanvasMobileMenu'),
      GamingWorld: () => import('@/components/GamingWorld'),
      LiveStream: () => import('@/components/LiveStream'),
      UpcomingMatchesHome: () => import('@/components/UpcomingMatchesHome'),
      CounterUp: () => import('@/components/CounterUp'),
      PopularGame: () => import('@/components/Games/PopularGame'),
      Testimonial: () => import('@/components/Testimonial'),
      BlogPost: () => import('@/components/BlogPost'),
      ContactBanner: () => import('@/components/ContactBanner'),
      Footer: () => import('@/components/Footer')
<<<<<<< HEAD
  },
=======
  }, 
>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b
  data() {
      return {
          navOpen: false,
          paddingTop: "pt-32"
      }
  },
}
</script>
