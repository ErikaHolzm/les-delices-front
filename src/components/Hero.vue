<template>
  <section id="inicio" class="relative h-screen flex items-center justify-center overflow-hidden">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <div class="w-full h-full bg-gradient-to-br from-verde-oscuro/80 to-verde-medio/80"></div>
      <img 
        src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
        alt="Cafetería elegante" 
        class="w-full h-full object-cover opacity-40"
      />
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white px-4 max-w-4xl mx-auto animate-fade-in">
      <h1 class="font-serif text-4xl md:text-6xl lg:text-7xl font-bold mb-6 text-shadow">
        Les Délices
      </h1>
      <p class="text-xl md:text-2xl mb-8 font-light text-dorado-claro">
        Una experiencia gastronómica única en la Rambla Punta del Este
      </p>
      <div class="space-y-4 md:space-y-0 md:space-x-4 md:flex md:justify-center">
        <a href="#productos" class="btn-secondary inline-block">
          Descubrir Nuestros Productos
        </a>
        <a href="#contacto" class="btn-primary inline-block">
          Reservar Mesa
        </a>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-10">
      <a href="#productos" class="text-white/70 hover:text-white transition-colors duration-300">
        <svg class="w-6 h-6 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
        </svg>
      </a>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this component
</script>

<style scoped>
.animate-fade-in {
  animation: fadeIn 1.2s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
