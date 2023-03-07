<template lang="">
  <div>
    <navLogin />
    <div class="w-full h-[640px] relative">
      <img src="./../assets/bg-login.jpg" alt="image" class="w-full h-full" />
      <div class="w-[420px] h-[360px] bg-white rounded-md shadow-lg absolute top-32 right-44">
        <div class="px-6 py-9">
          <h3 class="font-semibold text-2xl">Sign in</h3>
          <div class="mt-3">
            <label for="email" class="font-normal text-base">Email</label>
            <input v-model="email" type="email" id="email" placeholder="Enter Email" class="w-[380px] mt-2 py-2 px-2 border border-slate-300 rounded-md focus:ring-blue-500 focus:border-blue-500" />
          </div>
          <div class="mt-3">
            <label for="password" class="font-normal text-base">Password</label>
            <input v-model="password" type="password" id="password" placeholder="•••••••••" class="w-[380px] mt-2 py-2 px-2 border border-slate-300 rounded-md focus:ring-blue-500 focus:border-blue-500" />
          </div>
          <button @click="login" class="px-4 py-2 bg-[#29BAA3] text-white mt-3 rounded-md shadow-lg">Sign in</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import navLogin from "@/components/NavLogin.vue";

export default {
  components: {
    navLogin,
  },
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    async login() {
      const url = "http://cors-anywhere.herokuapp.com/http://interview.pluginesia.com/login";
      const data = `{
  	"email": "${this.email}",
    "password": "${this.password}"}`;

      const response = await fetch(url, {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: data,
      });

      const text = await response;
      const token = await response.text();
      console.log(text)
      console.log(token)
      if(response.status == 200) {
        localStorage.setItem('token', token)
        this.$router.push('/home')
      }else {
        console.log(text);
      }
    },
  },
};
</script>
<style></style>
