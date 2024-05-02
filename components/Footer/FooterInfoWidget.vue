<template>
    <div class="flex flex-col text-right mr-10	">
        <!-- Footer Logo Start -->
        <div class="footer-logo">
        <NuxtLink to="/" class="mb-10">
            <img class=" logo-fot rounded-2xl	 mb-6" src="/images/club-80.png" alt="Footer Logo" width="220" height="180" 	>
        </NuxtLink>
    </div>
        <!-- Footer Logo End -->

        <!-- Text Start -->
        <p dir="rtl" class="text-start text-xl">گیم نت <strong>club80</strong> .با ارائه پلی استیشن 5 و تلویزیون 4K  ومحیطی پر هیجان همراه با کافی شاپ آماده ساخت یک روز رویایی برای شماست</p>
        <!-- Text End -->
        <!-- Social Icon List Start -->
        <ul class="flex mt-4 justify-end">
            <li v-for="(link, index) in links" :key="index" class="mr-4 last:mr-0">
                <a :href="`${link.href}`"  class="w-10 h-10 leading-10 text-center inline-block" ><i :class="link.className"></i></a>
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
                        BgShape: "/images/icon/bg-icon.webp",
                        className: "icofont-whatsapp icon-color"
                    },
                    {
                        href: "https://youtube.com/@PlayStation?si=MQx4TZmrMy2dMxxs",
                        BgShape: "/images/icon/bg-icon.webp",
                        className: "icofont-youtube-play icon-color"
                    },
                  /*   {
                        href: "https://t.me/+989217913298",
                        BgShape: "/images/icon/bg-icon.webp",
                        className: "icofont-telegram icon-color"
                    }, */
                    {
                        href: "https://www.instagram.com/club80.game?igsh=ZjRoM21vNTN2Zm5i",
                        BgShape: "/images/icon/bg-icon.webp",
                        className: "icofont-instagram icon-color"
                    }
                ],

            }
        }
    }
</script>


<style scoped>
.icon-color{
    color: #150645d1;
    font-size: 25px;
   text-shadow: 0.5px 1px 0.5px;
    transition: all 0.2s;
    background-color:white ;
    padding: 10px;
    box-shadow: 9px -14px 15px 0px rgba(0,0,0,0.1);
    border-radius: 30% 70% 70% 30% / 30% 35% 65% 70% ;


}
.icon-color:hover{
    color: white;
    background-color:#150645d1 ;
    transition: all 0.2s;
    transform: scaleX(1.5);

}
</style>