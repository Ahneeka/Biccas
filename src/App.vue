<template>
  <div>
  <Navbar />
  <Hero />
  <Teams />
  </div>
</template>

<script>
import Navbar from '@/components/NavBar'
import Hero from '@/components/HeRo'
import Teams from "@/components/TeAms.vue"
export default {
  name: 'App',
  components: {
   Navbar,
   Hero,
   Teams
   
  }
}
</script>

<style>

</style>
