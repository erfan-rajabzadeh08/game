<template>
    <!-- Header Section Start -->
    <header class="fixed left-0 right-0 z-99" :class="{'is-sticky': isSticky}">
        <div class="container">
            <div class="flex header-home pt-8 py-3 items-center justify-between">

                <HeaderLogo/>

                <MainMenu/>

                <SignupButton/>

            </div>
        </div>
    </header>
    <!-- Header Section End -->
</template>

<script>
    export default {
        components: {
            HeaderLogo: () => import('@/components/Header/HeaderLogo'),
            MainMenu: () => import('@/components/Header/MainMenu'),
            SignupButton: () => import('@/components/Button/SignupButton'),
        },

        data() {
            return {
                isSticky: false,
            }
        },

        mounted(){
            window.addEventListener('scroll', () => {
                let scrollPos = window.scrollY
                if(scrollPos >= 100){
                    this.isSticky = true
                } else {
                    this.isSticky = false
                }
            })
        },
    };
</script>