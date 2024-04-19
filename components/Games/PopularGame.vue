<template>
    <div class="container mt-120 mb-120">
        <TitleSection :title="title" :text="text"/>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 2xl:grid-cols-2 gap-6">
            <div class="relative group before:empty-content before:absolute before:w-full before:h-full before:opacity-0 before:bg-black before:top-0 before:left-0 before:right-0 before:bottom-0 overflow-hidden hover:before:opacity-70 transition-all hover:before:transition-all before:border-4 before:border-white before:rounded-4xl before:border-opacity-20" v-for="(games, index) in gameHome.slice(0, 4)" :key="index">
                <img class="w-full rounded-4xl" :src="games.gameImage" alt="Feature Icon">
                <n-link :to="`/game/${games.slug}`" class="group btn-color primary-btn absolute-center opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all" >
                    <img src="/images/icon/arrrow-left-icon.webp" alt="Arrow Icon" class=" Aroww-icon w-4 h-4 group-hover:ml-4 transition-all">
                    {{games.btnName}}
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
                title: "بازی های محبوب مجموعه ما",
                text: "تعدادی از بازی های محبوب مجموعه ما را ببین و ساعتی رو با ارامش سپری کن"
            }
        }
    }
</script>

<style scoped>
.btn-color{
    background: rgb(27,0,65);
background: linear-gradient(330deg, rgba(27,0,65,1) 14%, rgba(98,18,132,1) 67%, rgba(29,1,67,1) 98%);
border-radius: 15px;
font-size: 19px;
width: 40%;
height: 65px;
}
.Aroww-icon{
    margin-right: 5px;
}
.group :hover{
    margin-right: 5px;

}

</style>
