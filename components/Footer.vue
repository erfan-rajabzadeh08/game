<template>
    <!-- Footer Section Start -->
    <div>

        <!-- Main Footer Start -->
        <div class="py-32">
            <div class="container">
                <div class="grid grid-cols-1 sm:grid-cols-12">

                    <div class="sm:col-span-12 lg:col-span-6 mt-10 sm:mt-0 ord3">
                        <FooterContactInfoWidget/>
                    </div>
                    <!-- <div class="sm:col-span-6 lg:col-span-3 mt-10 lg:mt-0">
                        <FooterWinnerWidget/>
                    </div> -->
                  <!--   <div class="sm:col-span-6 lg:col-span-4 mt-10 lg:mt-0 ord2">
                        <FooterMenuList/>
                    </div> -->
                    <div class="sm:col-span-12 lg:col-span-6 ord1 ">
                        <FooterInfoWidget/>
                    </div>
                </div>
            </div>
        </div>
        <!-- Main Footer End -->

        <!-- Footer Bottom Start -->
        <!-- <div class="bg-gray-800 py-5">

            <div class="container flex justify-between relative items-center md:flex-row flex-col-reverse">

                <p class="text-gray-500 text-sm uppercase font-medium mb-0">© 2021 BONX Made with <i class="icofont-heart text-primary"></i>  by <a href="https://hasthemes.com" class="transition-all hover:text-primary text-white">HasThemes</a></p>

                <client-only>
                    <back-to-top class="md:absolute-center position-absolute cursor-pointer z-999 left-3/4 md:left-1/2 mb-15 sm:mb-auto" bottom="auto" right="auto">
                        <img src="/images/icon/scroll-top.webp" alt="">
                    </back-to-top>
                </client-only>

                <ul class="flex">
                    <li v-for="(link, index) in links" :key="index" class="text-white content-last-child-before before:ml-3 before:mr-3 before:inline-block content-before" tw-content-last-child-before="||">
                        <n-link :to="`${link.pageLink}`" class="text-gray-500 text-sm uppercase font-medium transition-all hover:text-primary">{{link.linkName}}</n-link>
                    </li>
                </ul>

            </div>

        </div> -->
        <!-- Footer Bottom End -->

    </div>
    <!-- Footer Section End -->
</template>

<script>
    export default {
        components: {
            FooterInfoWidget: () => import('@/components/Footer/FooterInfoWidget'),
            FooterContactInfoWidget: () => import('@/components/Footer/FooterContactInfoWidget'),
/*             FooterWinnerWidget: () => import('@/components/Footer/FooterWinnerWidget'),
 */            FooterMenuList: () => import('@/components/Footer/FooterMenuList')
        },
        data() {
            return {
                links: [
                    {
                        contentBefore: "",
                        pageLink: "/contact",
                        linkName: "Terms & Condition"
                    },
                    {
                        contentBefore: "||",
                        pageLink: "/contact",
                        linkName: "Privacy Policy"
                    }
                ]
            }
        }
    }
</script>


<style scoped>
@media (max-width:1000px) {
.ord1{
    display: grid;
    order: 1 !important;
}
.ord2{
    display: grid;
    order: 2 !important;
}
.ord3{
    display: grid;
    order: 3 !important;
}
}
</style>
