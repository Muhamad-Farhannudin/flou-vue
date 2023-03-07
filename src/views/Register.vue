<template lang="">
  <div>
    <NavRegis />
    <div class="w-full h-[640px] relative">
      <img src="./../assets/bg-login.jpg" alt="image" class="w-full h-full" />
      <div class="w-[420px] h-[500px] bg-white rounded-md shadow-lg absolute top-28 right-44">
        <div class="px-6 py-9">
          <h3 class="font-semibold text-2xl">Register</h3>
          <div class="mt-3">
            <label for="email" class="font-normal text-base">Email</label>
            <input v-model="email" type="email" id="email" placeholder="Your Email" class="w-[380px] mt-2 py-2 px-2 border border-slate-300 rounded-md active:border-blue-500" />
          </div>

          <div class="mt-3">
            <label for="password" class="font-normal text-base">Password</label>
            <input v-model="password" type="password" id="password" placeholder="You password" class="w-[380px] mt-2 py-2 px-2 border border-slate-300 rounded-md focus:ring-blue-500 focus:border-blue-500" />
          </div>
          <div class="mt-3">
            <label for="password" class="font-normal text-base">Confrim Password</label>
            <input v-model="confirmPassword" type="password" id="password" placeholder="Confirm your password" class="w-[380px] mt-2 py-2 px-2 border border-slate-300 rounded-md focus:ring-blue-500 focus:border-blue-500" />
          </div>
          <button @click="register" class="px-4 py-2 bg-[#29BAA3] text-white mt-3 rounded-md shadow-lg hover:opacity-80 transition-all duration-300">Sign Up</button>
          <p class="font-light text-xs mt-3">
            Existing account,
            <router-link to="/login">
              <span class="text-[#29BAA3] hover:opacity-60 cursor-pointer transition-all duration-300">login now</span>
            </router-link>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import NavRegis from "@/components/NavRegis.vue";
import axios from "axios";
export default {
  components: {
    NavRegis,
  },
  data() {
    return {
      email: "",
      password: "",
      confirmPassword: "",
    };
  },
  methods: {
    async register() {
      const url = "https://cors-anywhere.herokuapp.com/http://interview.pluginesia.com/register";

      const data = `{
  	"email": "${this.email}",
    "password": "${this.password}",
    "confpassword": "${this.confirmPassword}"
}`;

      const response = await fetch(url, {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: data,
      });

      const text = await response;
      if(response.status == 201) {
        this.$router.push('/login')
      }else {
        console.log(text);
      }
    }
  },
};
</script>
<style></style>
