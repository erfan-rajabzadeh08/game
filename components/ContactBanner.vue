<template>
    <!-- Contact Banner Section Start -->
    <div class="container" :class="paddingTop">
        <div class="flex justify-center flex-row-reverse md:justify-around flex-col md:flex-row-reverse items-center bg-no-repeat bg-scroll bg-center bg-cover lg:px-100 px-10 h-300" :style="{backgroundImage: `url(${ videoBannerBg })`}">
            <div>
                <h2 class="text-white md:text-4xl lg:text-3xl xl: text-5xl  sm:text-3xl text-2xl text-center md:text-right mb-6 md:mb-0 uppercase font-bold leading-9 lg:leading-70">برای رزرو وقت <br> با ما در تماس باشید</h2>
            </div>
            <div>
                <n-link to="/contact" class="group primary-btn opacity-100 transition-all btn-color" >
                    <img src="/images/icon/arrrow-left-icon.webp" alt="Arrow Icon" class=" Aroww-icon ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                    {{btnName}}
                </n-link>
            </div>
        </div>
    </div>
    <!-- Contact Banner Section End -->
</template>

<script>
export default {
    props: {
        paddingTop: String,
    },
    data(){
        return {
            videoBannerBg: "/images/bg/gaming-update.webp",
            btnName: "ارتباط با ما"
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
}
.Aroww-icon{
    margin-right: 5px;
}
.group :hover{
    margin-right: 5px;

}

</style>
