<template>
  <div id="app">
    <Navbar />
    <Sidebar />
    <Main />
    <div class='main-section'>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>

import Navbar from "@/components/Navbar.vue";
import Sidebar from "@/components/Sidebar.vue";
import Main from "@/components/Main.vue";

export default {
  name: 'app',
  data() {

  },
  components: {
    Navbar,
    Sidebar,
    Main
  }
}
</script>

<style>

</style>
