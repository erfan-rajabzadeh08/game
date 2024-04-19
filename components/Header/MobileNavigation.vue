<template>
    <div class="mobile-navigation">
        <nav class="offcanvas-navigation" id="offcanvas-navigation">
            <ul>
                <li class="menu-item-has-children">
                    <n-link class=" text-white text-xl text-right font-semibold capitalize block pb-4 pt-4 pt- border-b-1 border-gray-200 transition-all hover:text-primary text-black text-dark" to="/">خانه </n-link>
                </li>
                <li class="menu-item-has-children">
                    <n-link class=" text-white text-xl text-right font-semibold capitalize block pb-4 pt-4 pt- border-b-1 border-gray-200 transition-all hover:text-primary text-black text-dark" to="/game">بازی ها</n-link>
                </li>
                <li class="menu-item-has-children ">
                    <n-link class=" text-white text-xl text-right font-semibold  capitalize block pb-4 pt-4 pt- border-b-1 border-gray-200 transition-all hover:text-primary text-black text-dark" to="/about">درباره ما </n-link>
                </li>
                <li class="menu-item-has-children ">
                    <n-link class=" text-white  text-xl text-right font-semibold capitalize block pb-4 pt-4 pt- border-b-1 border-gray-200 transition-all hover:text-primary text-black text-dark" to="/contact">ارتباط با ما </n-link>
                </li>

                <!-- <li class="menu-item-has-children relative block">
                    <n-link class="text-base text-white  font-semibold capitalize block pb-4 pt-4  border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/">Match</n-link>
                    <ul class="sub-menu ml-5">
                        <li>
                            <n-link class="text-white  text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/match">Match Page</n-link>
                        </li>
                        <li>
                            <n-link class="text-white  text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/match/1">Match Details</n-link>
                        </li>
                    </ul>
                </li> -->

             <!--    <li class="menu-item-has-children relative block">
                    <n-link class="text-white text-base font-semibold capitalize block pb-4 pt-4  border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/">Pages</n-link>
                    <ul class="sub-menu ml-5">
                        <li>
                            <n-link class="text-white  text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/about">About Us</n-link>
                        </li>
                        <li>
                            <n-link class="text-white  text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/game">All Games</n-link>
                        </li>
                        <li>
                            <n-link class="text-white  text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/game/1">Game Details</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/player">Players</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/player/1">Player Details</n-link>
                        </li>
                        <li>
                            <n-link class="text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/FAQ">FAQ</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/404Error">404-Error</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/signup">SignUp</n-link>
                        </li>
                    </ul>
                </li>
 -->
               <!--  <li class="menu-item-has-children relative block">
                    <n-link class=" text-white text-base font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog">Blog</n-link>
                    <ul class="sub-menu ml-5">
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-without-sidebar">Blog Without Sidebar Page</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-right-sidebar">Blog Right Sidebar</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-left-sidebar">Blog Left Sidebar</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-grid-right-sidebar">Blog Grid Right Sidebar</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-grid-left-sidebar">Blog Grid Left Sidebar</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog-grid-without-sidebar">Blog Grid Without Sidebar</n-link>
                        </li>
                        <li>
                            <n-link class=" text-white text-sm font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/blog/1">Blog Details</n-link>
                        </li>
                    </ul>
                </li> -->

              <!--   <li> -->
<!--                     <n-link class=" text-white text-base font-semibold capitalize block pb-4 pt-4 border-b-1 border-gray-200 transition-all hover:text-primary text-black" to="/contact">Contact Us</n-link>
 -->              <!--   </li> -->
            </ul>
        </nav>
    </div>
</template>

<script>
    export default{
        name: 'MobileNavMenu',
        mounted() {
            const offCanvasNav = document.querySelector('#offcanvas-navigation');
            const offCanvasNavSubMenu = offCanvasNav.querySelectorAll('.sub-menu');
            const anchorLinks = offCanvasNav.querySelectorAll('a');

            for (let i = 0; i < offCanvasNavSubMenu.length; i++){
                offCanvasNavSubMenu[i].insertAdjacentHTML("beforebegin", "<span class='menu-expand'><i class='plus-minus'></i></span>");
            }

            const menuExpand = offCanvasNav.querySelectorAll('.menu-expand');
            const numMenuExpand = menuExpand.length;

            for (let i = 0; i < numMenuExpand; i++) {
                menuExpand[i].addEventListener("click", (e) => {sideMenuExpand(e)});
            }

            for (let i = 0; i < anchorLinks.length; i++) {
                anchorLinks[i].addEventListener("click", () => {closeMobileMenu()});
            }

            const sideMenuExpand = (e) => {
                e.currentTarget.parentElement.classList.toggle('active');
            }
            const closeMobileMenu = () => {
                const offcanvasMobileMenu = document.querySelector('#offcanvas-mobile-menu');
                offcanvasMobileMenu?.classList.remove('active');
            }
        }
    };
</script>