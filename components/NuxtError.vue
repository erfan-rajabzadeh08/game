<template>
    <section class="py-10">
        <div class="container">
            <div class="error_inner text-center">

                <div class="title text-white mb-16">
                    <h3 class="sm:text-6xl text-4xl mb-5 font-bold">OPPS...</h3>
                    <p class="sm:text-4xl text-2xl uppercase font-bold">SORRY, this page is not found.</p>
                </div>

                <div class="error-404 mb-68">
                    <img src="/images/others/404.webp" alt="">
                </div>

                <div class="flex justify-center">
                    <n-link to="/" class="group primary-btn opacity-100 transition-all" style="background-image:url(/images/others/btn-bg.webp)">
                        <img src="/images/icon/arrrow-left-icon.webp" alt="Arrow Icon" class="mr-3 w-5 h-5 group-hover:mr-4 transition-all">
                        {{btnName}}
                    </n-link>
                </div>

            </div>
        </div>
    </section>
</template>

<script>
export default {
  data () {
      return {
        btnName: "Go to Home"
      }
  }
}
</script>