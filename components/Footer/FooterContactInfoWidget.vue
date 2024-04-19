<template>
    <div class="">
        <FooterWidgetTitle :title="title"/>
        <div class="flex flex-col mb-5 pr-5 xl:pr-0">
            <span class="text-primary mb-3">Location:</span>
            <p>136 Harding Ave Wheeling, West Virginia</p>
        </div>
        <div class="flex flex-col">
            <span class="text-primary mb-3">Phone:</span>
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
            title: "Contact",
            phone: "00 (62) 632 867 4497"
        }
    },
}
</script>