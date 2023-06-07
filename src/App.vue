<script setup>
import Navbar from "./components/Navbar.vue";
import Form from "./components/Form.vue";
</script>

<template>
  <v-app class="bg-app m-0 p-0">
    <Navbar></Navbar>
  <Form/>
    
  </v-app>
</template>
    
<script>
export default {

  data() {
    return {
      whatsapp: "https://web.whatsapp.com/",
    };
  },
};
</script>

<style scoped>
</style>