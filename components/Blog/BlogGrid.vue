<template>
    <div class="grid gap-10 xs:grid-cols-2 md:grid-cols-2 mt-8">
        <div class="single_blog items-center" v-for="(blog, index) in blogData" :key="index">
            <div class="blog_thumb">
                <n-link :to="`/blog/${blog.slug}`">
                    <img class="rounded-xl" :src="blog.blogGrid" :alt="blog.alt">
                </n-link>
            </div>
            <div class="blog_content mt-6">
                <span class="text-sm text-white font-exo font-normal mb-2 sm:mb-5 block"><i class="icofont-calendar text-primary mr-2"></i>{{blog.date}}</span>
                <h2 class="text-white xl:text-2xl lg:text-xl md:text-2xl sm:text-lg font-bold uppercase font-exo hover:text-primary transition-all mb-2 sm:mb-5 leading-9">
                    <n-link :to="`/blog/${blog.slug}`">{{blog.title}}</n-link>
                </h2>
                <n-link :to="`/blog/${blog.slug}`" class="uppercase font-exo relative pl-12 text-sm text-white transition-all hover:text-primary before:empty-content before:absolute before:h-0.5 before:w-7.5 before:bg-primary before:left-0 before:top-1/2 before:transform before:-translate-y-1/2">Read More</n-link>
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