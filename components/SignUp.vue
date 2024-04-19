<template>
    <!-- SignUp Section Start -->
    <div class="container">
        <form id="contact-form" class="flex flex-col max-w-lg mx-auto" action="">
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
                <input type="password" class="px-6 h-14 mb-6 text-white border-secondary-80 bg-secondary-100 hover:border-primary transition-all border-2 border-solid block rounded-md w-full focus:outline-none" placeholder="Password">
            </div>
            <div class="single-fild col-span-2">

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
    <!-- SignUp Section End -->
</template>

<script>
    export default {
        data() {
            return {
                btnName: "Register"
            }
        }
    }
</script>