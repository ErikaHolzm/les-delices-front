<template>
  <footer class="bg-verde-oscuro text-white">
    <div class="container mx-auto px-4 py-12">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Logo y Descripción -->
        <div class="space-y-4">
          <div class="flex items-center space-x-2">
            <div class="w-10 h-10 bg-dorado rounded-full flex items-center justify-center">
              <span class="text-verde-oscuro font-serif text-xl font-bold">L</span>
            </div>
            <span class="font-serif text-xl font-bold">Les Délices</span>
          </div>
          <p class="text-white/80 leading-relaxed">
            Confitería, restaurante y cafetería premium en la Rambla Punta del Este. 
            Una experiencia gastronómica única con productos artesanales.
          </p>
        </div>

        <!-- Enlaces Rápidos -->
        <div class="space-y-4">
          <h3 class="font-serif text-lg font-bold text-dorado">Enlaces Rápidos</h3>
          <ul class="space-y-2">
            <li>
              <a href="#inicio" class="text-white/80 hover:text-dorado transition-colors duration-300">
                Inicio
              </a>
            </li>
            <li>
              <a href="#productos" class="text-white/80 hover:text-dorado transition-colors duration-300">
                Productos
              </a>
            </li>
            <li>
              <a href="#historia" class="text-white/80 hover:text-dorado transition-colors duration-300">
                Nuestra Historia
              </a>
            </li>
            <li>
              <a href="#horarios" class="text-white/80 hover:text-dorado transition-colors duration-300">
                Horarios
              </a>
            </li>
            <li>
              <a href="#contacto" class="text-white/80 hover:text-dorado transition-colors duration-300">
                Contacto
              </a>
            </li>
          </ul>
        </div>

        <!-- Contacto -->
        <div class="space-y-4">
          <h3 class="font-serif text-lg font-bold text-dorado">Contacto</h3>
          <div class="space-y-2 text-white/80">
            <p class="flex items-center space-x-2">
              <svg class="w-4 h-4 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
              </svg>
              <span>Rambla Punta del Este 1234</span>
            </p>
            <p class="flex items-center space-x-2">
              <svg class="w-4 h-4 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
              </svg>
              <span>+598 42 44 1234</span>
            </p>
            <p class="flex items-center space-x-2">
              <svg class="w-4 h-4 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
              <span>info@lesdelices.com.uy</span>
            </p>
          </div>
        </div>
      </div>

      <!-- Bottom Footer -->
      <div class="border-t border-white/20 mt-12 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0">
          <p class="text-white/60 text-sm">
            © {{ currentYear }} Les Délices. Todos los derechos reservados.
          </p>
          <div class="flex space-x-6">
            <a href="#" class="text-white/60 hover:text-dorado transition-colors duration-300 text-sm">
              Política de Privacidad
            </a>
            <a href="#" class="text-white/60 hover:text-dorado transition-colors duration-300 text-sm">
              Términos y Condiciones
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const currentYear = ref(new Date().getFullYear())

onMounted(() => {
  currentYear.value = new Date().getFullYear()
})
</script>

<style scoped>
/* No additional styles needed */
</style>
