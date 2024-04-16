<template>
    <!-- Contact Form Section Start -->
    <div class="container">
        <!-- Title Section Start -->
        <TitleSection :title="title" :text="text"/>
        <!-- Title Section End -->

        <form id="contact-form" 
            class="grid sm:gap-x-8 gap-x-4 grid-cols-2" 
            action="https://getform.io/f/6af30b8c-e767-4d30-b964-d7e38d35078b" 
            method="POST">

            <div class="single-fild">
                <input type="text" class="px-6 h-14 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" placeholder="Name">
            </div>
            <div class="single-fild">
                <input type="email" class="px-6 h-14 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" placeholder="E-mail">
            </div>
            <div class="single-fild">
                <input type="text" class="px-6 h-14 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" placeholder="Phone">
            </div>
            <div class="single-fild">
                <input type="text" class="px-6 h-14 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" placeholder="Address">
            </div>
            <div class="single-fild col-span-2">
                <textarea class="px-6 pt-4 h-40 md:h-60 lg:h-72 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" type="text" placeholder="Write from here" spellcheck="false" data-gramm="false"></textarea>

                <div class="form-btn-wrap flex justify-center w-full mt-16">
                    <button type="submit" value="submit" name="submit" class="form-btn group primary-btn opacity-100 transition-all uppercase" style="background-image:url(/images/others/btn-bg.webp)">
                        {{btnName}}
                        <img src="/images/icon/arrrow-icon.webp" alt="Arrow Icon" class="ml-3 w-5 h-5 group-hover:ml-4 transition-all">
                    </button>
                    <p class="form-messege"></p>
                </div>
            </div>
        </form>

    </div>
    <!-- Contact Form Section End -->
</template>

<script>
    export default {
        components: {
            TitleSection: () => import('@/components/Title/TitleSection')
        },
        data() {
            return {
                title: "Get in Touch",
                text: "When unknown printer took type and scrambled it to make type specimen book centuries,",
                btnName: "Submit Now"
            }
        }
    }
</script>