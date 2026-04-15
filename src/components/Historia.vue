<template>
  <section id="historia" class="section-padding bg-crema">
    <div class="container mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Content -->
        <div class="animate-slide-up">
          <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl font-bold text-verde-oscuro mb-6">
            Nuestra Historia
          </h2>
          <div class="w-24 h-1 bg-dorado mb-8"></div>
          
          <div class="space-y-6 text-cafe/80">
            <p class="leading-relaxed">
              <span class="text-dorado font-serif text-xl font-bold">L</span>es Délices nació en 2018 de la pasión de dos hermanos por la gastronomía francesa y uruguaya. 
              Con una visión clara: crear un espacio donde la tradición artesanal se encuentre con la elegancia contemporánea.
            </p>
            
            <p class="leading-relaxed">
              Nuestro nombre, "Les Délices" (Los Deliciosos), refleja nuestro compromiso con cada detalle. 
              Desde la selección de granos de café hasta el horneado de nuestros croissants, cada proceso es 
              una celebración del sabor y la calidad.
            </p>
            
            <p class="leading-relaxed">
              Ubicados en la prestigiosa Rambla Punta del Este, hemos convertido nuestro local en un 
              refugio para quienes buscan más que un café: buscan una experiencia memorable, donde cada 
              visita es una invitación a disfrutar de los pequeños placeres de la vida.
            </p>
            
            <blockquote class="border-l-4 border-dorado pl-6 italic text-verde-oscuro/90 font-medium">
              "En Les Délices, cada taza de café cuenta una historia y cada postre es un poema."
            </blockquote>
          </div>

          <!-- Values -->
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-12">
            <div class="text-center">
              <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                </svg>
              </div>
              <h3 class="font-serif font-bold text-verde-oscuro mb-2">Calidad</h3>
              <p class="text-sm text-cafe/70">Ingredientes premium seleccionados con esmero</p>
            </div>
            
            <div class="text-center">
              <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                </svg>
              </div>
              <h3 class="font-serif font-bold text-verde-oscuro mb-2">Artesanía</h3>
              <p class="text-sm text-cafe/70">Elaboración tradicional y métodos caseros</p>
            </div>
            
            <div class="text-center">
              <div class="w-16 h-16 bg-verde-oscuro rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-dorado" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"/>
                </svg>
              </div>
              <h3 class="font-serif font-bold text-verde-oscuro mb-2">Pasión</h3>
              <p class="text-sm text-cafe/70">Amor por cada detalle y cada cliente</p>
            </div>
          </div>
        </div>

        <!-- Image -->
        <div class="relative animate-zoom-in">
          <div class="relative h-96 lg:h-full min-h-[400px] rounded-lg overflow-hidden shadow-2xl">
            <img 
              src="https://images.unsplash.com/photo-1554118811-1e0d58224f24?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" 
              alt="Interior de Les Délices" 
              class="w-full h-full object-cover transition-transform duration-700 hover:scale-105"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-verde-oscuro/30 to-transparent"></div>
          </div>
          
          <!-- Decorative Element -->
          <div class="absolute -bottom-6 -right-6 w-32 h-32 bg-dorado/20 rounded-full -z-10"></div>
          <div class="absolute -top-6 -left-6 w-24 h-24 bg-verde-oscuro/10 rounded-full -z-10"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this component
</script>

<style scoped>
.animate-slide-up {
  animation: slideUp 0.8s ease-out;
}

.animate-zoom-in {
  animation: zoomIn 0.8s ease-out;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes zoomIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}
</style>
