<template>
    <!-- Breadcrumb Start -->
    <div class="flex items-center relative bg-no-repeat bg-scroll bg-center bg-cover lg:mb-32 md:mb-20 mb-15 h-365 md:h-460 lg:h-500" style="background-image:url(/images/bg/breadcrumbs-bg.webp);">
        <div class="container">
            <div class="relative 2xl:pt-20 lg:pt-16 pt-12 md:mb-12 z-10 flex flex-col justify-center items-center text-center">

                <h1 class="text-white font-metal uppercase font-normal lg:text-5.5xl md:text-7xl text-5xl tracking-wide mb-6 text-shadow" v-if="BreadcrumbTitle">{{BreadcrumbTitle}}</h1>

                <ul class="flex">
                    <li>
                        <n-link class="text-white uppercase text-base sm:text-lg font-bold mr-2 transition-all hover:text-primary" to="/">Home</n-link>
                    </li>
                    <li>
                        <span class="text-white uppercase text-base sm:text-lg font-bold mr-2">//</span>
                    </li>
                    <li>
                        <span class="text-primary uppercase text-base sm:text-lg font-bold" v-if="BreadcrumbSubTitle">{{BreadcrumbSubTitle}}</span>
                    </li>
                </ul>


            </div>
        </div>
    </div>
    <!-- Breadcrumb End -->
</template>

<script>
    export default {
        props: {
            BreadcrumbTitle: {
                type: String,
                required: false,
            }, 
            BreadcrumbSubTitle: {
                type: String,
                required: false,
            }
        },
        components: {
        }
    };
</script>