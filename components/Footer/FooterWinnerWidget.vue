<template>
    <div class=" mr-8">
<<<<<<< HEAD
     <!--    <FooterWidgetTitle :title="title"/> -->
<!--
=======
        <FooterWidgetTitle :title="title"/>

>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b
        <div class="grid grid-cols-3 sm:grid-cols-3 gap-3">
            <n-link v-for="(match, index) in matches" :key="index" to="/player">
                <img :src="`${match.gamingBg}`" :alt="match.gamingAlt">
            </n-link>
<<<<<<< HEAD
        </div> -->
=======
        </div>
>>>>>>> 994ec5da85c7a0d07412275aa72d7f316cca830b
    </div>
</template>
<script>
export default {
    components:{
        FooterWidgetTitle: () => import('@/components/Footer/FooterWidgetTitle'),
    },
    data () {
        return {
            title: "today’s winners",
            matches: [
                {
                    gamingBg: "/images/others/winners1.webp",
                    gamingAlt: "Winner"
                },
                {
                    gamingBg: "/images/others/winners2.webp",
                    gamingAlt: "Winner"
                },
                {
                    gamingBg: "/images/others/winners3.webp",
                    gamingAlt: "Winner"
                },
                {
                    gamingBg: "/images/others/winners4.webp",
                    gamingAlt: "Winner"
                },
                {
                    gamingBg: "/images/others/winners5.webp",
                    gamingAlt: "Winner"
                },
                {
                    gamingBg: "/images/others/winners6.webp",
                    gamingAlt: "Winner"
                }
            ]
        }
    },
}
</script>