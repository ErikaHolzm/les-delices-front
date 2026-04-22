# Imágenes de Productos - Les Délices

## Estructura de archivos

Coloca tus imágenes locales en esta carpeta con los siguientes nombres:

- `croissant.jpg` - Croissant Artesanal
- `cafe.jpg` - Café Especial Les Délices  
- `tarta-limon.jpg` - Tarta de Limón
- `sandwich.jpg` - Sandwich Gourmet
- `chocolate.jpg` - Chocolate Caliente
- `muffin.jpg` - Muffin de Arándanos

## Cómo usar imágenes locales

1. Coloca tus archivos de imagen en esta carpeta
2. Descomenta las líneas de importación en `src/components/Productos.vue`:

```javascript
// Importar imágenes locales
import croissantImage from '@/assets/images/croissant.jpg'
import cafeImage from '@/assets/images/cafe.jpg'
import tartaLimonImage from '@/assets/images/tarta-limon.jpg'
import sandwichImage from '@/assets/images/sandwich.jpg'
import chocolateImage from '@/assets/images/chocolate.jpg'
import muffinImage from '@/assets/images/muffin.jpg'
```

3. Reemplaza las URLs en el array de productos:

```javascript
const productos = ref([
  {
    nombre: "Croissant Artesanal",
    descripcion: "...",
    precio: "450",
    imagen: croissantImage  // <- Usar import local
  },
  // ... demás productos
])
```

## Beneficios de usar imágenes locales

- **Carga más rápida**: No dependen de conexiones externas
- **Sin errores**: Las imágenes siempre estarán disponibles
- **Offline**: El sitio funciona sin conexión a internet
- **Control total**: Tienes control sobre la calidad y tamaño

## Especificaciones recomendadas

- **Formato**: JPG o WebP
- **Dimensiones**: 800x600px (o proporción 4:3)
- **Calidad**: 80-90% (balance calidad/tamaño)
- **Peso**: Máximo 200KB por imagen
