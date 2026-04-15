<template>
  <section id="contacto" class="section-padding bg-crema">
    <div class="container mx-auto">
      <!-- Header -->
      <div class="text-center mb-12">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl font-bold text-verde-oscuro mb-4">
          Contacto
        </h2>
        <p class="text-lg text-cafe/80 max-w-2xl mx-auto mb-6">
          Estamos ubicados en el corazón de la Rambla Punta del Este. Te esperamos para vivir una experiencia única
        </p>
        <div class="w-24 h-1 bg-dorado mx-auto"></div>
      </div>

      <!-- Contact Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 max-w-6xl mx-auto">
        <!-- Mapa y Dirección -->
        <div class="space-y-6">
          <div class="bg-white rounded-lg shadow-lg p-6 card-hover">
            <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4 flex items-center">
              <svg class="w-6 h-6 text-dorado mr-3" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
              </svg>
              Ubicación
            </h3>
            <p class="text-cafe/80 leading-relaxed">
              Rambla Punta del Este 1234<br>
              Maldonado, Uruguay<br>
              <span class="text-dorado font-medium">A pasos del mar</span>
            </p>
          </div>

          <div class="bg-white rounded-lg shadow-lg p-6 card-hover">
            <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4 flex items-center">
              <svg class="w-6 h-6 text-dorado mr-3" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
              </svg>
              Teléfono
            </h3>
            <p class="text-cafe/80">
              <a href="tel:+59842441234" class="hover:text-dorado transition-colors duration-300">
                +598 42 44 1234
              </a><br>
              <a href="tel:+59891234567" class="hover:text-dorado transition-colors duration-300">
                +598 91 234 567 (WhatsApp)
              </a>
            </p>
          </div>

          <div class="bg-white rounded-lg shadow-lg p-6 card-hover">
            <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-4 flex items-center">
              <svg class="w-6 h-6 text-dorado mr-3" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
              Email
            </h3>
            <p class="text-cafe/80">
              <a href="mailto:info@lesdelices.com.uy" class="hover:text-dorado transition-colors duration-300">
                info@lesdelices.com.uy
              </a>
            </p>
          </div>

          <!-- Mapa Placeholder -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden h-64">
            <div class="w-full h-full bg-gradient-to-br from-verde-oscuro/20 to-dorado/20 flex items-center justify-center">
              <div class="text-center">
                <svg class="w-16 h-16 text-verde-oscuro mx-auto mb-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                </svg>
                <p class="text-verde-oscuro font-medium">Mapa interactivo</p>
                <p class="text-cafe/70 text-sm">Rambla Punta del Este 1234</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Información de Reservas -->
        <div class="bg-white rounded-lg shadow-lg p-8">
          <h3 class="font-serif text-2xl font-bold text-verde-oscuro mb-6 text-center">
            Reservas
          </h3>
          
          <div class="space-y-6">
            <div class="text-center">
              <p class="text-cafe/80 mb-6">
                Para hacer una reserva, contáctanos directamente por WhatsApp o teléfono.
              </p>
              <div class="bg-dorado/10 rounded-lg p-6 border border-dorado/30">
                <h4 class="font-serif text-lg font-bold text-verde-oscuro mb-4 text-center">
                  Horarios de Atención
                </h4>
                <div class="space-y-2 text-cafe/80 text-center">
                  <p><span class="font-medium">Lunes a Viernes:</span> 7:00 - 23:00</p>
                  <p><span class="font-medium">Sábados y Domingos:</span> 8:00 - 22:00</p>
                </div>
              </div>
            </div>

            <div class="text-center">
              <a 
                href="https://wa.me/59891234567?text=Hola%20Les%20Délices!%20Quisiera%20hacer%20una%20reserva."
                target="_blank"
                rel="noopener noreferrer"
                class="btn-secondary"
              >
                Reservar por WhatsApp
              </a>
            </div>
          </div>
        </div>
      </div>

      <!-- Redes Sociales -->
      <div class="mt-16 text-center">
        <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-6">
          Síguenos en nuestras redes
        </h3>
        <div class="flex justify-center space-x-6">
          <a href="#" class="w-12 h-12 bg-verde-oscuro rounded-full flex items-center justify-center text-white hover:bg-dorado transition-colors duration-300">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
            </svg>
          </a>
          <a href="#" class="w-12 h-12 bg-verde-oscuro rounded-full flex items-center justify-center text-white hover:bg-dorado transition-colors duration-300">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 110 6.666 3.333 3.333 0 010-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this component
</script>

<style scoped>
/* No additional styles needed */
</style>
