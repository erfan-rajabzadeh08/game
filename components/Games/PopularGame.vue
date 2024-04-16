<template>
    <div class="container mb-120">
        <TitleSection :title="title" :text="text"/>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 2xl:grid-cols-2 gap-6">
            <div class="relative group before:empty-content before:absolute before:w-full before:h-full before:opacity-0 before:bg-black before:top-0 before:left-0 before:right-0 before:bottom-0 overflow-hidden hover:before:opacity-70 transition-all hover:before:transition-all before:border-4 before:border-white before:rounded-4xl before:border-opacity-20" v-for="(games, index) in gameHome.slice(0, 4)" :key="index">
                <img class="w-full rounded-4xl" :src="games.gameImage" alt="Feature Icon">
                <n-link :to="`/game/${games.slug}`" class="group primary-btn absolute-center opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all" style="background-image:url(/images/others/btn-bg.webp)">
                    {{games.btnName}}
                    <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                </n-link>
            </div>
        </div>
    </div>
</template>
<script>
    import gameHome from '@/data/games.json'
    export default {
        components: {
            TitleSection: () => import('@/components/Title/TitleSection'),
        },
        data () {
            return {
                gameHome,
                title: "Popular Game",
                text: "When unknown printer took type and scrambled it to make type specimen book centuries,"
            }
        }
    }
</script>