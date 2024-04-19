<template>
    <div class="text-center lg:mb-15 md:mb-12 mb-8">
        <h2 class="text-white font-exo font-bold uppercase xl:text-title lg:text-5xl md:text-4xl sm:text-3xl text-2xl xl:leading-70 lg:leading-12 leading-10 max-w-sm md:max-w-xl lg:max-w-2xl mx-auto" v-if="title"> {{title}} </h2>
        <p class="max-w-lg text-gray-100 mx-auto text-base sm:text-lg leading-8 mt-3" v-if="text"> {{text}} </p>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: false,
        }, 
        text: {
            type: String,
            required: false,
        }
    }
}
</script>