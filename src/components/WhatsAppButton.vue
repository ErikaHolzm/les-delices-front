<template>
  <a 
    href="https://wa.me/59891234567?text=Hola%20Les%20Délices!%20Quisiera%20hacer%20una%20reserva."
    target="_blank"
    rel="noopener noreferrer"
    class="whatsapp-float"
    :class="{ 'scrolled': isScrolled }"
    aria-label="Contactar por WhatsApp"
  >
    <svg 
      viewBox="0 0 448 512" 
      fill="currentColor"
      class="w-6 h-6"
    >
      <path d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.8 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.4 0-65.7-8.8-94.3-25.5l-6.8-4-70.8 18.6 18.9-69.1-4.4-7c-17.6-29.8-27-64.1-27-100.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 54 81.2 54 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.6 19.1-19.6 46.6 0 27.5 20.1 54.1 22.9 57.9 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"/>
    </svg>
  </a>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 100
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.whatsapp-float {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 70px;
  height: 70px;
  background-color: #25D366;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 6px 20px rgba(37, 211, 102, 0.5);
  transition: all 0.3s ease;
  z-index: 1000;
  text-decoration: none;
  border: 3px solid white;
}

.whatsapp-float:hover {
  transform: scale(1.15);
  box-shadow: 0 8px 30px rgba(37, 211, 102, 0.7);
  background-color: #128C7E;
}

.whatsapp-float.scrolled {
  bottom: 40px;
  transform: scale(0.95);
}

.whatsapp-float.scrolled:hover {
  transform: scale(1.1);
}

.whatsapp-float svg {
  width: 32px;
  height: 32px;
}

@media (max-width: 640px) {
  .whatsapp-float {
    width: 60px;
    height: 60px;
    bottom: 20px;
    right: 20px;
  }
  
  .whatsapp-float svg {
    width: 28px;
    height: 28px;
  }
}

@media (max-width: 480px) {
  .whatsapp-float {
    width: 55px;
    height: 55px;
    bottom: 15px;
    right: 15px;
  }
  
  .whatsapp-float svg {
    width: 26px;
    height: 26px;
  }
}
</style>
