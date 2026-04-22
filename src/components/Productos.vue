<template>
  <section id="productos" class="section-padding bg-white">
    <div class="container mx-auto">
      <!-- Header -->
      <div class="text-center mb-16 animate-slide-up">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl font-bold text-verde-oscuro mb-4">
          Nuestros Productos
        </h2>
        <p class="text-lg text-cafe/80 max-w-2xl mx-auto">
          Descubre nuestra selección de productos artesanales, elaborados con los mejores ingredientes y mucho amor
        </p>
        <div class="w-24 h-1 bg-dorado mx-auto mt-6"></div>
      </div>

      <!-- Product Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div 
          v-for="(producto, index) in productos" 
          :key="index"
          class="producto-card card-hover bg-crema rounded-lg overflow-hidden shadow-lg animate-slide-up"
          :style="{ animationDelay: `${index * 100}ms` }"
        >
          <!-- Image Container -->
          <div class="relative h-64 overflow-hidden group">
            <img 
              :src="producto.imagen" 
              :alt="producto.nombre"
              class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
              @error="handleImageError"
              :data-producto-nombre="producto.nombre"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </div>

          <!-- Content -->
          <div class="p-6">
            <h3 class="font-serif text-xl font-bold text-verde-oscuro mb-3">
              {{ producto.nombre }}
            </h3>
            <p class="text-cafe/70 mb-4 leading-relaxed">
              {{ producto.descripcion }}
            </p>
            <div class="flex justify-between items-center">
              <span class="text-dorado font-bold text-lg">
                ${{ producto.precio }}
              </span>
              <button class="btn-secondary text-sm px-4 py-2">
                Ordenar
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Call to Action -->
      <div class="text-center mt-16">
        <a href="#contacto" class="btn-primary">
          Consultar Nuestro Menú Completo
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// Importar todas las imágenes locales
import croissantImage from '@/assets/images/2290d1c1-d10a-4c76-8366-1e9cf40f9b46_16-9-aspect-ratio_default_0.jpg'
import cafeImage from '@/assets/images/descarga.webp'
import tartaLimonImage from '@/assets/images/baked-lemon-tart-85811-1.webp'
import sandwichImage from '@/assets/images/hq720.jpg'
import chocolateImage from '@/assets/images/shutterstock_1665115558-1024x683.jpg'
import muffinImage from '@/assets/images/03COOKING-JORDANMARSHMUFFIN2-threeByTwoMediumAt2X-v2.jpg'

// URLs verificadas y funcionales de comida real
const productos = ref([
  {
    nombre: "Croissant Artesanal",
    descripcion: "Hojaldre francés crujiente con mantequilla premium, horneado diariamente. Perfecto con nuestro café especial.",
    precio: "450",
    imagen: sandwichImage
  },
  {
    nombre: "Café Especial Les Délices",
    descripcion: "Blend exclusivo de granos seleccionados, con notas chocolatosas y final frutal. Tostado en nuestro local.",
    precio: "280",
    imagen: cafeImage
  },
  {
    nombre: "Tarta de Limón",
    descripcion: "Postre clásico con base de masa sable, crema de limón fresca y merengue torrado. Un equilibrio perfecto de dulce y ácido.",
    precio: "680",
    imagen: tartaLimonImage
  },
  {
    nombre: "Sandwich Gourmet",
    descripcion: "Pan artesanal de masa madre, relleno con ingredientes premium de temporada. Acompañado de ensalada fresca.",
    precio: "890",
    imagen: croissantImage
  },
  {
    nombre: "Chocolate Caliente",
    descripcion: "Elaborado con chocolate belga 70% cacao, espeso y cremoso. Decorado con crema chantilly y virutas de chocolate.",
    precio: "420",
    imagen: chocolateImage
  },
  {
    nombre: "Muffin de Arándanos",
    descripcion: "Esponjoso muffin con arándanos frescos, cubierto con streusel de avena. Perfecto para el desayuno o merienda.",
    precio: "320",
    imagen: muffinImage
  }
])

// Placeholder image para errores
const placeholderImage = "https://picsum.photos/seed/lesdelices-placeholder/800/600.jpg"

// Manejo de errores en imágenes con múltiples niveles de respaldo
const handleImageError = (event) => {
  const img = event.target
  const productName = img.dataset.productoNombre
  
  console.warn(`Error cargando imagen para: ${productName}`)
  
  // Nivel 1: Placeholders específicos por producto
  const specificPlaceholders = {
    "Tarta de Limón": "https://picsum.photos/seed/tarta-limon/800/600.jpg",
    "Muffin de Arándanos": "https://picsum.photos/seed/muffin-arandanos/800/600.jpg"
  }
  
  // Nivel 2: Placeholder genérico
  const genericPlaceholder = "https://picsum.photos/seed/lesdelices-placeholder/800/600.jpg"
  
  // Nivel 3: Imagen base64 simple (comida genérica)
  const base64Placeholder = "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='600' viewBox='0 0 800 600'%3E%3Crect fill='%23f5f5f5' width='800' height='600'/%3E%3Ctext x='50%25' y='50%25' font-family='Arial' font-size='24' fill='%23666' text-anchor='middle' dy='.3em'%3EImagen no disponible%3C/text%3E%3C/svg%3E"
  
  // Intentar con placeholder específico primero
  if (!img.dataset.errorAttempted) {
    img.dataset.errorAttempted = 'true'
    const specificPlaceholder = specificPlaceholders[productName]
    if (specificPlaceholder) {
      img.src = specificPlaceholder
      return
    }
  }
  
  // Segundo intento: placeholder genérico
  if (!img.dataset.genericAttempted) {
    img.dataset.genericAttempted = 'true'
    img.src = genericPlaceholder
    return
  }
  
  // Último recurso: SVG base64
  img.src = base64Placeholder
}
</script>

<style scoped>
.animate-slide-up {
  animation: slideUp 0.6s ease-out forwards;
  opacity: 0;
}

@keyframes slideUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
  from {
    opacity: 0;
    transform: translateY(30px);
  }
}
</style>
