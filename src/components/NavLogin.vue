<template lang="">
    <div class="max-w-full px-20 py-3 bg-dark-green">
        <div class="flex justify-between text-white">
            <Logo />
            <div class="flex items-center px-3">
                <div class="w-5 h-5 ">
                    <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M21 12C21 16.9706 16.9706 21 12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3C16.9706 3 21 7.02944 21 12Z" stroke="#fff" stroke-width="2"></path> <path d="M12 3.05554C14.455 5.25282 16 8.44597 16 12C16 15.554 14.455 18.7471 12 20.9444" stroke="#fff" stroke-width="2" stroke-linecap="round"></path> <path d="M12.0625 21C9.57126 18.8012 8 15.5841 8 12C8 8.41592 9.57126 5.19883 12.0625 3" stroke="#fff" stroke-width="2" stroke-linecap="round"></path> <path d="M3 12H21" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
                </div>
                <p class="px-1 font-normal text-base ">English</p>
                <div class="w-5 h-5">
                    <svg fill="#fff" viewBox="0 0 1024 1024" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M759.2 419.8L697.4 358 512 543.4 326.6 358l-61.8 61.8L512 667z"></path></g></svg>
                </div>
                <router-link to="/">
                    <button class="px-3 font-normal text-base">Sign Up</button>
                </router-link>
            </div>
        </div>
    </div>
</template>
<script>
import Logo from "@/components/Logo.vue";

export default {
    components: {
        Logo,
    }
}
</script>
<style>
    
</style>