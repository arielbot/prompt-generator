<template>
    <div class="body-bg min-h-screen px-2 md:px-0">
      <Navbar />
      <Headermain />
      <Nuxt />
    </div>
</template>

<script>
import Navbar from '~/components/NavBar.vue'
import Headermain from '~/components/HeaderMain.vue'

export default {
    components: {
      Navbar,
      Headermain
    }
  }
</script>

<style scoped>
.body-bg {
    background-color: #D9AFD9;
    background-image: linear-gradient(0deg, #D9AFD9 0%, #97D9E1 100%);
  }
</style>
