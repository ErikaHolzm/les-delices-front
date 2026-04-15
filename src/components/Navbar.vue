<template>
  <header class="fixed top-0 w-full bg-crema/95 backdrop-blur-custom shadow-md z-50 transition-all duration-300" :class="{ 'py-2': isScrolled, 'py-4': !isScrolled }">
    <nav class="container mx-auto px-4 flex justify-between items-center">
      <!-- Logo -->
      <div class="flex items-center space-x-2">
        <div class="w-10 h-10 bg-verde-oscuro rounded-full flex items-center justify-center">
          <span class="text-dorado font-serif text-xl font-bold">L</span>
        </div>
        <span class="font-serif text-xl font-bold text-verde-oscuro">Les Délices</span>
      </div>

      <!-- Desktop Navigation -->
      <ul class="hidden md:flex space-x-8">
        <li>
          <a href="#inicio" class="nav-link text-verde-oscuro hover:text-dorado transition-colors duration-300 font-medium">
            Inicio
          </a>
        </li>
        <li>
          <a href="#productos" class="nav-link text-verde-oscuro hover:text-dorado transition-colors duration-300 font-medium">
            Productos
          </a>
        </li>
        <li>
          <a href="#historia" class="nav-link text-verde-oscuro hover:text-dorado transition-colors duration-300 font-medium">
            Nuestra Historia
          </a>
        </li>
        <li>
          <a href="#horarios" class="nav-link text-verde-oscuro hover:text-dorado transition-colors duration-300 font-medium">
            Horarios
          </a>
        </li>
        <li>
          <a href="#contacto" class="nav-link text-verde-oscuro hover:text-dorado transition-colors duration-300 font-medium">
            Contacto
          </a>
        </li>
      </ul>

      <!-- Mobile Menu Button -->
      <button 
        @click="toggleMobileMenu" 
        class="md:hidden text-verde-oscuro hover:text-dorado transition-colors duration-300"
        aria-label="Toggle mobile menu"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </nav>

    <!-- Mobile Menu -->
    <div v-if="mobileMenuOpen" class="md:hidden bg-crema/95 backdrop-blur-custom border-t border-verde-oscuro/20">
      <ul class="py-4 space-y-2">
        <li>
          <a href="#inicio" @click="closeMobileMenu" class="block px-4 py-2 text-verde-oscuro hover:bg-dorado/10 hover:text-dorado transition-colors duration-300">
            Inicio
          </a>
        </li>
        <li>
          <a href="#productos" @click="closeMobileMenu" class="block px-4 py-2 text-verde-oscuro hover:bg-dorado/10 hover:text-dorado transition-colors duration-300">
            Productos
          </a>
        </li>
        <li>
          <a href="#historia" @click="closeMobileMenu" class="block px-4 py-2 text-verde-oscuro hover:bg-dorado/10 hover:text-dorado transition-colors duration-300">
            Nuestra Historia
          </a>
        </li>
        <li>
          <a href="#horarios" @click="closeMobileMenu" class="block px-4 py-2 text-verde-oscuro hover:bg-dorado/10 hover:text-dorado transition-colors duration-300">
            Horarios
          </a>
        </li>
        <li>
          <a href="#contacto" @click="closeMobileMenu" class="block px-4 py-2 text-verde-oscuro hover:bg-dorado/10 hover:text-dorado transition-colors duration-300">
            Contacto
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const mobileMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.nav-link {
  position: relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #d4af37;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}
</style>
