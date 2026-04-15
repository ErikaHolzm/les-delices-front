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

const productos = ref([
  {
    nombre: "Croissant Artesanal",
    descripcion: "Hojaldre francés crujiente con mantequilla premium, horneado diariamente. Perfecto con nuestro café especial.",
    precio: "450",
    imagen: "https://images.unsplash.com/photo-1559329007-40df8a9345d8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  },
  {
    nombre: "Café Especial Les Délices",
    descripcion: "Blend exclusivo de granos seleccionados, con notas chocolatosas y final frutal. Tostado en nuestro local.",
    precio: "280",
    imagen: "https://images.unsplash.com/photo-1559056199-641a07c9a180?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  },
  {
    nombre: "Tarta de Limón",
    descripcion: "Postre clásico con base de masa sable, crema de limón fresca y merengue torrado. Un equilibrio perfecto de dulce y ácido.",
    precio: "680",
    imagen: "https://images.unsplash.com/photo-1568957441955-2903642d3d73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  },
  {
    nombre: "Sandwich Gourmet",
    descripcion: "Pan artesanal de masa madre, relleno con ingredientes premium de temporada. Acompañado de ensalada fresca.",
    precio: "890",
    imagen: "https://images.unsplash.com/photo-1528735602780-2552fd46c7af?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  },
  {
    nombre: "Chocolate Caliente",
    descripcion: "Elaborado con chocolate belga 70% cacao, espeso y cremoso. Decorado con crema chantilly y virutas de chocolate.",
    precio: "420",
    imagen: "https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  },
  {
    nombre: "Muffin de Arándanos",
    descripcion: "Esponjoso muffin con arándanos frescos, cubierto con streusel de avena. Perfecto para el desayuno o merienda.",
    precio: "320",
    imagen: "https://images.unsplash.com/photo-1606313564200-e75d5e476c8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80"
  }
])
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
