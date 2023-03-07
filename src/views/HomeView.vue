<template>
  <div>
    <h1 v-if="error">
      <div class="w-1/3 bg-dark-green mt-5 mx-auto text-center rounded-lg shadow-xl">
        <h3 class="font-semibold text-white pt-5">Anda belum Login, silahkan login terlebih dahulu</h3>
        <div class="flex items-center justify-center mt-5 py-4">
          <router-link to="/login">
            <button class="px-3 py-2 font-normal text-base bg-[#88c102] rounded-lg text-white hover:opacity-60 duration-300">Login</button>
          </router-link>
          <p class="font-normal text-white ml-3">Atau</p>
          <router-link to="/">
            <button class="px-3 py-2 font-normal text-base bg-white rounded-lg text-[#88c102] ml-6 shadow-md hover:opacity-60 duration-300">Register</button>
          </router-link>
        </div>
      </div>
    </h1>
    <div v-else>
      <Navbar />
      <FlouCloud :data="data" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Navbar from "./../components/Navbar.vue";
import FlouCloud from "./../components/FlouCloud.vue";
import Footer from "./../components/Footer.vue";
export default {
  components: {
    Navbar,
    FlouCloud,
    Footer,
  },
  data() {
    return {
      data: "",
      error: false,
    };
  },
  methods: {
    async getData() {},
  },
  async mounted() {
    if (localStorage.getItem("token")) {
      this.error = false;
      const url = "http://cors-anywhere.herokuapp.com/http://interview.pluginesia.com/jsonTest";

      const response = await fetch(url, {
        headers: {
          Authorization: "Bearer " + localStorage.getItem("token"),
        },
      });

      const text = await response.json();
      this.data = text.product;
      console.log(this.data);
    } else {
      this.error = true;
    }
  },
  async created() {
    let status = "";
    // axios.get('https://cors-anywhere.herokuapp.com/http://interview.pluginesia.com/me', {
    //   headers: {
    //     Authorization: 'Bearer ' + localStorage.getItem('token')
    //   }
    // }).then(function (response) {
    //   status = response.statusText
    //   console.log(response)
    // }).catch(function(error) {
    // if (error.response.status == 400 || error.response.status == 401) {
    //   this.error = true;
    // }
    //   console.log(error)
    // })
    // if(status == 'ok') {
    // }
    this.getData();
  },
};
</script>
