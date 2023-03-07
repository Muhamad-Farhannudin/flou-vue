<template lang="">
  <div class="max-w-full px-20 py-5 mx-1 mb-1 bg-dark-green">
    <div class="flex justify-between text-white">
      <Logo />
      <div class="flex w-[35%]">
        <div class="w-8 h-8 bg-white rounded-full flex items-center justify-center mr-5 cursor-pointer transition-all hover:translate-y-1 duration-300">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path opacity="0.1" d="M17 10C17 13.866 13.866 17 10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10Z" fill="#323232"></path>
              <path d="M15 15L21 21" stroke="#323232" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
              <path d="M17 10C17 13.866 13.866 17 10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10Z" stroke="#323232" stroke-width="2"></path>
            </g>
          </svg>
        </div>
        <div class="w-40 flex items-center justify-center border border-white rounded-xl px-2 mr-5 cursor-pointer">
          <div class="w-6 h-6">
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier">
                <path d="M4 7.00005L10.2 11.65C11.2667 12.45 12.7333 12.45 13.8 11.65L20 7" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
                <rect x="3" y="5" width="18" height="14" rx="2" stroke="#fff" stroke-width="2" stroke-linecap="round"></rect>
              </g>
            </svg>
          </div>
          <p class="px-1 font-light text-base ml-3">Contact Us</p>
        </div>
        <div class="w-32 flex items-center justify-between border border-white rounded-xl px-2 mr-5 cursor-pointer">
          <img src="./../assets/flag.png" alt="flag" class="w-6 h-4" />
          <p class="px-1 font-light text-base">English</p>
          <div class="w-5 h-5">
            <svg fill="#fff" viewBox="0 0 1024 1024" xmlns="http://www.w3.org/2000/svg">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier"><path d="M759.2 419.8L697.4 358 512 543.4 326.6 358l-61.8 61.8L512 667z"></path></g>
            </svg>
          </div>
        </div>
        <router-link to="/login">
          <button class="px-3 py-1 font-normal text-base bg-[#88c102] rounded-lg hover:opacity-90 duration-300">Login</button>
        </router-link>
      </div>
    </div>
  </div>
  <!--  -->
  <div class="max-w-full px-20 py-5 mx-1 bg-dark-green">
    <div class="flex justify-between text-white">
      <div class="flex items-center w-[60%] justify-between">
        <div class="flex items-center cursor-pointer hover:text-[#88c102] transition-all duration-300" @click="changeNav('whyflou')">
          <button>Why Flou</button>
          <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" fill="#fff" xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path
                d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
                fill="#fff"
              ></path>
            </g>
          </svg>
        </div>
        <div class="flex items-center cursor-pointer">
          <button class="hover:text-[#88c102] transition-all duration-300 ml-3">Products</button>
          <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" fill="#fff" xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path
                d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
                fill="#fff"
              ></path>
            </g>
          </svg>
        </div>
        <div class="flex items-center cursor-pointer">
          <button class="hover:text-[#88c102] transition-all duration-300 ml-3">Solution</button>
          <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" fill="#fff" xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path
                d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
                fill="#fff"
              ></path>
            </g>
          </svg>
        </div>
        <div class="flex items-center cursor-pointer">
          <button class="hover:text-[#88c102] transition-all duration-300 ml-3">Parteners</button>
          <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" fill="#fff" xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path
                d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
                fill="#fff"
              ></path>
            </g>
          </svg>
        </div>
        <div class="flex items-center cursor-pointer">
          <button class="hover:text-[#88c102] transition-all duration-300 ml-3">Pricing</button>
          <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" fill="#fff" xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <path
                d="M17.9188 8.17969H11.6888H6.07877C5.11877 8.17969 4.63877 9.33969 5.31877 10.0197L10.4988 15.1997C11.3288 16.0297 12.6788 16.0297 13.5088 15.1997L15.4788 13.2297L18.6888 10.0197C19.3588 9.33969 18.8788 8.17969 17.9188 8.17969Z"
                fill="#fff"
              ></path>
            </g>
          </svg>
        </div>
        <button class="ml-3 hover:text-[#88c102] transition-all duration-300">Resource</button>
        <button class="ml-3 hover:text-[#88c102] transition-all duration-300">Support</button>
        <button class="ml-3 hover:text-[#88c102] transition-all duration-300">Marketplace</button>
      </div>
      <button class="px-3 py-1 font-normal text-base bg-[#88c102] rounded-lg">Lets Get Started</button>
    </div>
  </div>
  <div class="max-w-full px-1 relative">
    <div class="relative">
      <img class="w-full -z-10" src="./../assets/image-home.jpg" alt="img-home" />
      <div class="w-full h-full absolute top-0 bg-black/40"></div>
    </div>
    <div class="absolute top-0 mt-28 ml-28">
      <h1 class="font-normal text-5xl text-white">FLOU Cloud Product</h1>
      <div class="w-1/2 mt-3">
        <p class="font-normal text-xl text-white">Explore FLOU Cloud's expanding range of high-performance cloud products including large-scale computing, storage resources, and Big Data processing capabilities for users around the world.</p>
      </div>
      <div class="flex mt-10">
        <button class="px-3 py-2 font-normal text-base bg-[#88c102] rounded-lg text-white hover:opacity-60 duration-300">Get Strated for Free</button>
        <button class="px-3 py-2 font-normal text-base bg-white rounded-lg text-[#88c102] ml-6 shadow-md hover:opacity-60 duration-300">Contact Sales</button>
      </div>
    </div>
  </div>
</template>
<script>
import Logo from "@/components/Logo.vue";
export default {
  components: {
    Logo,
  },
  data() {
    return {
      selectedNav: "",
    };
  },
  methods: {},
};
</script>
<style></style>
