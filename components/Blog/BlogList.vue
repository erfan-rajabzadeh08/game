<template>
    <!-- Blog Post Section Start -->
    <section class="container">

        <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-2 2xl:grid-cols-2 gap-12 px-0">
            <div v-for="(blog, index) in blogData" :key="index">
                <div class="flex sm:items-center flex-col sm:flex-row">
                    <div class="lg:w-40 xl:w-52 2xl:w-52 md:w-44 sm:w-37 w-32 mb-7 sm:mb-0 flex-shrink-0">
                        <n-link :to="`/blog/${blog.slug}`"><img :src="blog.imgSrc" :alt="blog.alt"></n-link>
                    </div>
                    <div class="xl:ml-9 lg:ml-6 md:ml-9 ml-3 flex flex-col flex-1">
                        <span class="text-sm text-white font-exo font-normal mb-2 sm:mb-5"><i class="icofont-calendar text-primary mr-2"></i>{{blog.date}}</span>
                        <h2 class="text-white xl:text-2xl lg:text-xl md:text-2xl sm:text-lg font-bold uppercase font-exo hover:text-primary transition-all mb-2 sm:mb-5 leading-9">
                            <n-link :to="`/blog/${blog.slug}`">{{blog.title}}</n-link>
                        </h2>
                        <n-link :to="`/blog/${blog.slug}`" class="uppercase font-exo relative pl-12 text-sm text-white transition-all hover:text-primary before:empty-content before:absolute before:h-0.5 before:w-7.5 before:bg-primary before:left-0 before:top-1/2 before:transform before:-translate-y-1/2">Read More</n-link>
                    </div>
                </div>
            </div>
        </div>

    </section>
    <!-- Blog Post Section End -->
</template>

<script>
  import blogData from '@/data/blog.json'
    export default {
        data() {
            return {
                blogData
            }
        }
    }
</script>