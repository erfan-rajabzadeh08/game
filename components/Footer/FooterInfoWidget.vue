<template>
    <div class="flex flex-col text-right mr-10	">
        <!-- Footer Logo Start -->
        <div class="footer-logo">
        <NuxtLink to="/" class="mb-10">
            <img class=" logo-fot rounded-2xl	 mb-6" src="/images/logo1.jpg" alt="Footer Logo" width="90" height="90" 	>
        </NuxtLink>
    </div>
        <!-- Footer Logo End -->

        <!-- Text Start -->
        <p class="text-start">گیم نت <strong>club80</strong> .با ارائه پلی استیشن 5  ومحیطی پر هیجان همراه با کافی شاپ آماده ساخت یک روز رویایی برای شماست</p>
        <!-- Text End -->
        <!-- Social Icon List Start -->
        <ul class="flex mt-4 justify-end">
            <li v-for="(link, index) in links" :key="index" class="mr-4 last:mr-0">
                <a :href="`${link.href}`" :style="{backgroundImage: `url(${ link.BgShape })`}" class="w-10 h-10 leading-10 text-center inline-block" ><i :class="link.className"></i></a>
            </li>
        </ul>
        <!-- Social Icon List End -->
    </div>
</template>

<script>
    export default {
        data() {
            return {
                links: [

                    {
                        href: "https://wa.me/9217913298" ,
                        BgShape: "/images/icon/watsap.webp",
                        className: "icofont-whatsapp text-white"
                    },
                    {
                        href: "https://youtube.com/@PlayStation?si=MQx4TZmrMy2dMxxs",
                        BgShape: "/images/icon/youtobe-bg.webp",
                        className: "icofont-youtube-play text-white"
                    },
                    {
                        href: "https://t.me/+989217913298",
                        BgShape: "/images/icon/telegram.webp",
                        className: "icofont-telegram text-white"
                    },
                    {
                        href: "https://www.instagram.com/club80.game?igsh=ZjRoM21vNTN2Zm5i",
                        BgShape: "/images/icon/instagram.webp",
                        className: "icofont-instagram text-white"
                    }
                ]
            }
        }
    }
</script>


<style scoped>
.logo-fot{
    mix-blend-mode: lighten;
}
</style>