<template>
    <!-- Faq Accordion Start  -->
    <div class="container overflow-hidden">
        <ul>
            <li v-for="(category, index) in paginatedOrders" :key="index" @click="visible=index" class="text-white cursor-pointer border-2 border-secondary-80 py-7 px-8 md:px-12 rounded-xl mb-7 text-lg md:text-2xl font-bold uppercase">
                {{ category.title }}
                <div class="cursor-text text-base capitalize text-gray-300 font-normal leading-8 mt-5" v-show="visible===index">
                    <p>{{ category.text }}</p>
                </div>
            </li>
        </ul>
    </div>
    <!-- Faq Accordion End -->
</template>

<script>
    export default {
        name: "trial-page",
        data() {
            return {
                paginatedOrders: [
                    {
                        title: "How can i contact the team for healp?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "What should I do if I’m missing a part?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "Can I play bonx more than once?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "What should I do if I’m missing a part?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "Are there any expansion packs on the way?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "Can I play bonx more than once?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "What should I do if I’m missing a part?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    },
                    {
                        title: "Are there any expansion packs on the way?",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been industry standard unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five reIcentem with desktop publishing softwa like including versions has been industry standard unknown printer took a galley of type and scramIblrd it to make a type specimen book ha with desktop publishing software like including versions."
                    }
                ],
                visible: null
            }
        }
    };
</script>

<style>
</style>
