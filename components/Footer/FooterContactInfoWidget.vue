<template>
    <div class="mr-10 ">
        <FooterWidgetTitle :title="title"/>
        <div class="flex flex-col mb-5  text-right  xl:pr-0">
            <span class="text-primary mb-3  text-2xl">:آدرس</span>
            <p class="text-xl">کرمان - رفسنجان خیابان اندیشه نبش کوچه 17</p>
        </div>
        <div class="flex flex-col text-right ">
            <span class="text-primary mb-3">:شماره تماس</span>
            <a :href="`tel:${phone}`" class="text-white hover:text-primary transition-all">{{phone}}</a>
        </div>
    </div>
</template>
<script>
export default {
    components:{
        FooterWidgetTitle: () => import('@/components/Footer/FooterWidgetTitle'),
    },
    data () {
        return {
            title: "",
            phone: "09217913298"
        }
    },
}
</script>
