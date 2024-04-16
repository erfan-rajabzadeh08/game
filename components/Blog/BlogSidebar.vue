<template>
    <div class="post-sidebar mt-8">
        <div class="px-5 md:px-4 lg:px-7 xl:px-9 py-7 border-secondary-80 bg-secondary-100 border-2 border-solid rounded-lg mb-10 last:mb-0">
            <h3 class="uppercase font-bold text-xl sm:text-2xl mb-7">Search Here</h3>
            <form action="#" class="relative">
                <input class="px-5 pr-16 h-14 border-secondary-80 bg-secondary-100 border-2 border-solid rounded-md w-full focus:outline-none" placeholder="Search here" type="text">
                <button type="submit" class="absolute px-5 top-0 right-0 bg-primary hover:bg-secondary-80 transition-all rounded-md inline-block h-full"><i class="icofont-search-1"></i></button>
            </form>
        </div>
        <div class="px-5 md:px-4 lg:px-7 xl:px-9 py-7 border-secondary-80 bg-secondary-100 border-2 border-solid rounded-lg mb-10 last:mb-0">
            <h3 class="uppercase font-bold text-xl sm:text-2xl mb-7">POST CATEGORY</h3>
            <ul>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Legendary</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Animation Game</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Offline Game</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Game Tata</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Single Player</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>Game Parady</n-link>
                </li>
                <li class="mb-5 last:mb-0">
                    <n-link to="#" class="px-5 py-4 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none"><i class="icofont-rounded-double-right"></i>ES Sports</n-link>
                </li>
            </ul>
        </div>
        <div class="px-5 md:px-4 lg:px-7 xl:px-9 py-7 border-secondary-80 bg-secondary-100 border-2 border-solid rounded-lg mb-10 last:mb-0">
            <h3 class="uppercase font-bold text-xl sm:text-2xl mb-7">TAGS</h3>
            <div class="all-tags">
                <n-link to="#" v-for="(blog, index) in blogData" :key="index" class="inline-block mr-2 my-1 border-secondary-80 bg-secondary-100 hover:bg-primary hover:border-primary transition-all border-2 border-solid rounded-lg py-3 px-6 xl:px-8">{{blog.tag}}</n-link>
            </div>
        </div>
    </div>
</template>
<script>
import blogData from '@/data/blog.json'
export default {
    data() {
        return {
            blogData
        }
    },
}
</script>