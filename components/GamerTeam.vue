<template>
    <!-- Blog Post Section Start -->
    <div class="container pt-32">

        <!-- Title Section Start -->
        <TitleSection :title="title" :text="text"/>
        <!-- Title Section End -->
        
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
            <div class="relative group w-300 sm:w-full mx-auto" v-for="(service, index) in services" :key="index">
                <div>
                    <img :src="service.imgSrc" :alt="service.alt">
                </div>
                <div class="flex flex-col justify-center items-center absolute bottom-0 left-0 right-0 bg-team-shape bg-cover h-24 sm:h-20 md:h-28 lg:h-24 xl:h-32 2xl:h-32 group-hover:bg-team-hover-shape hover:transition-all">
                    <h3 class="text-white font-bold text-lg md:text-2xl uppercase mb-2 xl:mb-4 leading-tight">{{service.name}}</h3>
                    <span class="text-primary text-sm md:text-base group-hover:text-white transition-all">{{service.subtitle}}</span>
                </div>
            </div>
        </div>

    </div>
    <!-- Blog Post Section End -->
</template>

<script>
    export default {
        components: {
            TitleSection: () => import('@/components/Title/TitleSection')
        },
        data() {
            return {
                title: "Meet Gamer Team",
                text: "When unknown printer took type and scrambled it to make type specimen book centuries",
                services: [
                    {
                        imgSrc: "/images/others/team1.webp",
                        alt: "Service Image",
                        name: "Tasia Mancuso",
                        subtitle: "SEO & Founder",
                    },
                    {
                        imgSrc: "/images/others/team2.webp",
                        alt: "Service Image",
                        name: "Rosaline Emmons",
                        subtitle: "Team Leader",
                    },
                    {
                        imgSrc: "/images/others/team3.webp",
                        alt: "Service Image",
                        name: "Willbarn Beharn",
                        subtitle: "Team Member"
                    }
                ]
            }
        }
    }
</script>