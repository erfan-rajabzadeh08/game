<template>
    <!-- CounterUp Section Start -->
    <div class="container mt-32 pb-32">
        <div v-observe-visibility="{callback: visibilityChanged, once: true}">
            <div v-if="commentsVisible" class="grid md:grid-cols-4 grid-cols-2 gap-9">
                <div v-for="(count, imageIndex) in counter" :key="imageIndex"  class="text-white text-center">
                    <countTo class="text-white text-5xl lg:text-10xl uppercase font-metal font-normal block" :class="count.className" :startVal='count.startVal' :endVal='count.endVal' :duration='3000' :autoplay='true'></countTo>
                    <p class="uppercase mt-3 sm:mt-5 text-base lg:text-lg">{{count.text}}</p>
                </div>
            </div>
        </div>
    </div>
    <!-- CounterUp Section End -->
</template>

<script>
    import countTo from 'vue-count-to';
    export default {
        components: {
            countTo
        },
        data () {
            return {
                commentsVisible: false,
                counter: [
                    {
                        startVal: 0,
                        endVal: 8697,
                        className: "text-yellow",
                        text: "Twitch Streams"
                    },
                    {
                        startVal: 0,
                        endVal: 480,
                        className: "text-bright",
                        text: "Total Games"
                    },
                    {
                        startVal: 0,
                        endVal: 5367,
                        className: "text-punch",
                        text: "Youtube Streams"
                    },
                    {
                        startVal: 0,
                        endVal: 249,
                        className: "text-primary",
                        text: "Pro Team"
                    }
                ]
            }
        },
        methods: {
            visibilityChanged(isVisible) {
                this.commentsVisible = isVisible;
            },
        }
    }
</script>