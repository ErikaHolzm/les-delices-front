<template>
  <section id="horarios" class="section-padding bg-white">
    <div class="container mx-auto">
      <!-- Header -->
      <div class="text-center mb-12">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl font-bold text-verde-oscuro mb-4">
          Horarios de Atención
        </h2>
        <p class="text-lg text-cafe/80 max-w-2xl mx-auto mb-6">
          Te esperamos para disfrutar de nuestra experiencia gastronómica en los horarios más convenientes
        </p>
        <div class="w-24 h-1 bg-dorado mx-auto"></div>
      </div>

      <!-- Horarios Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-4xl mx-auto">
        <!-- Café y Desayuno -->
        <div class="horario-card card-hover bg-crema rounded-lg p-8 text-center shadow-lg">
          <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-6">
            <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
              <path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z"/>
            </svg>
          </div>
          <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4">
            Café y Desayuno
          </h3>
          <div class="space-y-2 text-cafe/80">
            <p class="font-medium">Lunes a Viernes</p>
            <p class="text-dorado font-bold">7:00 - 12:00</p>
            <p class="font-medium mt-4">Sábados y Domingos</p>
            <p class="text-dorado font-bold">8:00 - 13:00</p>
          </div>
        </div>

        <!-- Almuerzo -->
        <div class="horario-card card-hover bg-crema rounded-lg p-8 text-center shadow-lg">
          <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-6">
            <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/>
            </svg>
          </div>
          <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4">
            Almuerzo
          </h3>
          <div class="space-y-2 text-cafe/80">
            <p class="font-medium">Lunes a Sábado</p>
            <p class="text-dorado font-bold">12:00 - 16:00</p>
            <p class="font-medium mt-4">Domingos</p>
            <p class="text-dorado font-bold">12:00 - 15:00</p>
          </div>
        </div>

        <!-- Merienda y Cena -->
        <div class="horario-card card-hover bg-crema rounded-lg p-8 text-center shadow-lg">
          <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-6">
            <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
              <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"/>
            </svg>
          </div>
          <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4">
            Merienda y Cena
          </h3>
          <div class="space-y-2 text-cafe/80">
            <p class="font-medium">Martes a Sábado</p>
            <p class="text-dorado font-bold">16:00 - 23:00</p>
            <p class="font-medium mt-4">Domingos</p>
            <p class="text-dorado font-bold">16:00 - 22:00</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this component
</script>

<style scoped>
.horario-card {
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.horario-card:hover {
  border-color: #d4af37;
  transform: translateY(-4px);
}
</style>
