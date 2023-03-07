<template lang="">
  <div class="w-full h-[1000px] mx-2 px-20 flex gap-x-28 pt-7">
    <div class="w-max">
      <h3 class="font-normal text-[#88c102] text-lg">{{data.title}}</h3>
      <div class="flex flex-col border-l border-gray-300 mt-5">
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] cursor-pointer hover:border-l hover:border-[#88c102] pl-3 w-max">Infrastructure as a Service</p>
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] hover:border-l hover:border-[#88c102] cursor-pointer pl-3">Software as a Service</p>
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] hover:border-l hover:border-[#88c102] cursor-pointer pl-3">Platform as a Service</p>
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] hover:border-l hover:border-[#88c102] cursor-pointer pl-3">Hybrid Multicloud</p>
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] hover:border-l hover:border-[#88c102] cursor-pointer pl-3">Services</p>
        <p class="font-normal text-lg text-gray-400 hover:text-[#88c102] hover:border-l hover:border-[#88c102] cursor-pointer pl-3">Private Cloud</p>
      </div>
    </div>
    <div class="w-full px-5 pt-4">
      <div class="relative">
        <input type="text" class="w-full py-2 bg-gray-100 border border-gray-200 rounded-md pl-5" placeholder="Search Product" />
        <div class="absolute right-3 top-3">
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
      </div>
      <hr class="mt-4">
      <h3 class="font-normal text-xl text-[#88c102] underline mt-5">Explore Infrastructure as a Service Productts (IaaS)</h3>
      <p class="font-normal text-gray-400">Helping to accelerate the business through strong and resilient infrastructure for unlimited customer <span class="block">experience.</span></p>
      <div class="flex mt-10 gap-7">
          <div class="w-full">
              <h3 class="font-medium text-xl text-[#88c102]">{{data['product-data']?.item[0]?.product[0]?.category}}</h3>
              <div class="w-3/4 h-[2px] mt-3 bg-gray-300"></div>
              <div v-for="(item,index) in data['product-data']?.item[0]?.product[0]?.item" class="flex mt-8 items-center hover:bg-gray-200 cursor-pointer duration-300">
                <div class="w-10 h-10 p-6 rounded-full bg-slate-300 shadow-lg"></div>
                <div class="ml-6">
                    <h2 class="font-medium text-xl text-[#88c102]">{{item.title}}</h2>
                    <p class="font-normal text-gray-400">{{item.desc}}</p>
                </div>
              </div>
          </div>
          <div class="w-full">
              <h3 class="font-medium text-xl text-[#88c102]">{{data['product-data']?.item[0]?.product[1]?.category}}</h3>
              <div class="w-3/4 h-[2px] mt-3 bg-gray-300"></div>
              <div class="w-[80%] flex mt-8 items-center hover:bg-gray-200 cursor-pointer duration-300" v-for="(item,index) in data['product-data']?.item[0]?.product[1]?.item">
                <div class="w-10 h-10 p-6 rounded-full bg-slate-300 shadow-lg"></div>
                <div class="ml-6">
                    <h2 class="font-medium text-xl text-[#88c102]">{{item.title}}</h2>
                    <p class="font-normal text-gray-400">{{item.desc}}</p>
                </div>
              </div>

              <div class="w-full mt-10">
                  <h3 class="font-medium text-xl text-[#88c102]">{{data['product-data']?.item[0]?.product[2]?.category}}</h3>
                  <div class="w-3/4 h-[2px] mt-3 bg-gray-300"></div>
                  <div class="w-[80%] flex mt-8 items-center hover:bg-gray-200 cursor-pointer duration-300" v-for="(item,index) in data['product-data']?.item[0]?.product[2]?.item">
                    <div class="w-10 h-10 p-6 rounded-full bg-slate-300 shadow-lg"></div>
                    <div class="ml-6">
                        <h2 class="font-medium text-xl text-[#88c102]">{{item.title}}</h2>
                        <p class="font-normal text-gray-400">{{item.desc}}</p>
                    </div>
                  </div>
              </div>
          </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ['data']
};
</script>
<style lang=""></style>
