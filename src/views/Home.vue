<template>
  <div class="home">
    <Hero />
    <Productos />
    <Historia />
    <Horarios />
    <Contacto />
  </div>
</template>

<script setup>
import Hero from '../components/Hero.vue'
import Productos from '../components/Productos.vue'
import Historia from '../components/Historia.vue'
import Horarios from '../components/Horarios.vue'
import Contacto from '../components/Contacto.vue'
</script>

<style scoped>
.home {
  width: 100%;
}
</style>
