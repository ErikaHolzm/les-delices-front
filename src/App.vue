<template>
  <div id="app" class="min-h-screen">
    <Navbar />
    <main>
      <router-view />
    </main>
    <Footer />
    <WhatsAppButton />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import WhatsAppButton from './components/WhatsAppButton.vue'
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;
}
</style>
