<template>
    <!-- Button Start -->
    <NuxtLink to="/game"  class=" btn-background w-230 md:text-2xl md:leading-12 h-16 flex items-center text-white font-bold justify-center font-exo group hover:opacity-80 leading-70 text-xl">
        <img class="mr-3 w-5 h-5 group-hover:ml-4 transition-all" src="/images/icon/arrrow-left-icon.webp" alt="Arrow Icon">
        مشاهده بازی ها
    </NuxtLink>
    <!-- Button End -->
</template>


<style scoped>
.btn-background{
border-radius: 10px;
padding: 8px !important;
margin: 5px !important;
background: rgb(164,50,241);
background: linear-gradient(210deg, rgba(164,50,241,1) 21%, rgba(95,0,158,1) 67%);
}
</style>