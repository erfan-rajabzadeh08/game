<template>
    <!-- All Games Start -->
    <div class="container mb-120">

        <div class="filter-wrap bg-secondary-100 rounded-2xl px-5 py-7 mb-10">
            <div class="flex flex-col sm:flex-row justify-between">
                <div class="category-filter">
                    <div class="filter-option">
                        <select id="selectgame" class="px-5 h-14 w-full mb-8 sm:mb-0 sm:w-64 text-white bg-secondary-100 border-2 border-solid rounded-lg focus:outline-none border-gray-400 block"> 
                            <option value="" class="bg-black">All Category</option>
                            <option value="1">Drawing</option>
                            <option value="2">Alien Space</option>
                            <option value="3">Hunter Sniper</option>
                            <option value="4">Collage</option>
                            <option value="5">Game one</option>
                        </select>
                    </div>
                </div>
                <div class="search-filter">
                    <div class="search-bx">
                        <form action="#" class="relative">
                            <input type="text" placeholder="Search" class="px-5 h-14 w-full sm:w-64 bg-secondary-100 border-2 border-solid rounded-lg focus:outline-none">
                            <button type="submit" class="absolute px-5 top-0 right-0 bg-transparent transition-all inline-block h-full text-white hover:text-primary">
                                <i class="icofont-search-1"></i>
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 2xl:grid-cols-2 gap-6 item-display">
            <div class="item relative group before:empty-content before:absolute before:w-full before:h-full before:opacity-0 before:bg-black before:top-0 before:left-0 before:right-0 before:bottom-0 overflow-hidden hover:before:opacity-70 transition-all hover:before:transition-all before:border-4 before:border-white before:rounded-4xl before:border-opacity-20" v-for="(games, index) in gameHome" :key="index">
                <img class="w-full rounded-4xl" :src="games.gameImage" alt="Feature Icon">
                <n-link :to="`/game/${games.slug}`" class="group primary-btn absolute-center opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all" style="background-image:url(/images/others/btn-bg.webp)">
                    {{games.btnName}}
                    <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                </n-link>
            </div>
        </div>
    </div>
    <!-- All Games End -->
</template>
<script>
    import gameHome from '@/data/games.json'
    export default {
        data () {
            return {
                gameHome,
            }
        }
    }
</script>