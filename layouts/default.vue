<template>
  <div class="w-full bg-gray-100">
    <Navbar />
    <Nuxt />
  </div>
</template>
<script>
import '~/assets/css/main.css'
import Navbar from '~/components/Navbar'
export default {
  components: {
    Navbar,
  },
}
</script>
