<template>
    <div class="flex flex-col mr-12 xl:mr-100">
        <!-- Footer Logo Start -->
        <NuxtLink to="/" class="mb-10">
            <img src="/images/logo.webp" alt="Footer Logo">
        </NuxtLink>
        <!-- Footer Logo End -->

        <!-- Text Start -->
<<<<<<< HEAD
        <p class="text-start">گیم نت <strong>club80</strong> با ارائه پلی استیشن 5  ومحیطی پر هیجان همراه با کافی شاپ آ»اده ساخت یک روز رویایی برای شماست</p>
        <!-- Text End -->
=======
        <p>It long estabhed fact that reader will ditracted the readable content looking using readable.</p>
        <!-- Text End -->

>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b
        <!-- Social Icon List Start -->
        <ul class="flex mt-4">
            <li v-for="(link, index) in links" :key="index" class="mr-4 last:mr-0">
                <a :href="`${link.href}`" :style="{backgroundImage: `url(${ link.BgShape })`}" class="w-10 h-10 leading-10 text-center inline-block"><i :class="link.className"></i></a>
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
                        href: "https://www.facebook.com",
                        BgShape: "/images/icon/facebook-bg.webp",
                        className: "icofont-facebook text-white"
                    },
                    {
                        href: "https://www.dribble.com",
                        BgShape: "/images/icon/dribble.webp",
                        className: "icofont-dribbble text-white"
                    },
                    {
                        href: "https://www.youtube.com",
                        BgShape: "/images/icon/youtobe-bg.webp",
                        className: "icofont-youtube-play text-white"
                    },
                    {
                        href: "https://www.twitter.com",
                        BgShape: "/images/icon/twittre.webp",
<<<<<<< HEAD
                        className: "icofont-telegram text-white"
=======
                        className: "icofont-twitter text-white"
>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b
                    }
                ]
            }
        }
    }
</script>