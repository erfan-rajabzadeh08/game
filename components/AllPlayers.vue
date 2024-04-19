<template>
    <!-- Blog Post Section Start -->
    <div class="container">
        
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
            <div class="relative group w-300 sm:w-full mx-auto" v-for="(player, index) in playerData" :key="index">
                <div class="w-full rounded-4xl overflow-hidden relative">
                    <img :src="player.imgSrc" :alt="player.alt">
                    <n-link :to="`/player/${player.slug}`" class="w-full h-full absolute left-0 top-0 bg-gray-900 rounded-5xl opacity-0 group-hover:opacity-70 border-4 border-gray-400 rounded-4xl"></n-link>
                    <ul class="social-link absolute left-0 text-center bottom-0 group-hover:bottom-8 w-full space-x-2 opacity-0 group-hover:opacity-100 transition-all z-20 text-white">
                        <li class="text-center inline-block">
                            <a href="https://www.twitch.tv" class="w-12 h-10 flex items-center justify-center transition-all bg-cover text-white hover:bg-arrow-shape bg-arrow-hover-shape z-50">
                                <i class="icofont-twitch"></i>
                            </a>
                        </li>
                        <li class="text-center inline-block">
                            <a href="https://www.facebook.com" class="w-12 h-10 flex items-center justify-center transition-all bg-cover text-white hover:bg-arrow-shape bg-arrow-hover-shape z-50">
                                <i class="icofont-facebook"></i>
                            </a>
                        </li>
                        <li class="text-center inline-block">
                            <a href="https://www.youtube.com" class="w-12 h-10 flex items-center justify-center transition-all bg-cover text-white hover:bg-arrow-shape bg-arrow-hover-shape z-50">
                                <i class="icofont-youtube-play"></i>
                            </a>
                        </li>
                        <li class="text-center inline-block">
                            <a href="https://www.twitter.com" class="w-12 h-10 flex items-center justify-center transition-all bg-cover text-white hover:bg-arrow-shape bg-arrow-hover-shape z-50">
                                <i class="icofont-twitter"></i>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="flex flex-col justify-center items-center mt-8 bg-team-shape bg-cover h-24 sm:h-20 md:h-28 lg:h-24 xl:h-32 2xl:h-32 group-hover:bg-team-hover-shape hover:transition-all">
                    <h3 class="text-white font-bold text-lg md:text-2xl uppercase mb-2 xl:mb-4 leading-tight">
                        <n-link :to="`/player/${player.slug}`">{{player.name}}</n-link>
                    </h3>
                    <span class="text-white text-sm group-hover:text-white transition-all">{{player.subtitle}}</span>
                </div>
            </div>
        </div>

    </div>
    <!-- Blog Post Section End -->

</template>

<script>
import playerData from '@/data/player.json'
    export default {
        components: {
        },
        data() {
            return {
                playerData
            }
        }
    }
</script>