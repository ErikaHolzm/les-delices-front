# Les Délices - Sitio Web Oficial

Sitio web informativo para la confitería, restaurante y cafetería Les Délices.

## Descripción

Proyecto desarrollado con Vue 3 + Vite + TailwindCSS que presenta una experiencia gastronómica premium con diseño elegante y optimizado para SEO.

## Características

- **Diseño Responsive**: Mobile-first, adaptable a todos los dispositivos
- **SEO Optimizado**: Meta tags, estructura semántica HTML5, headings correctos
- **Animaciones Suaves**: Efectos hover, transiciones y animaciones CSS
- **Componentes Reutilizables**: Arquitectura modular con Vue 3 Composition API
- **Paleta de Colores Elegante**: Verde oscuro y dorado como colores principales
- **Navegación Intuitiva**: Scroll suave entre secciones

## Secciones

1. **Navbar**: Navegación fija con logo y menú responsive
2. **Hero**: Sección principal con imagen de fondo y llamada a la acción
3. **Productos**: Galería de productos con cards interactivas
4. **Historia**: Storytelling sobre el local y sus valores
5. **Horarios**: Información de atención por categorías
6. **Contacto**: Rreservas e información de contacto
7. **Footer**: Información básica y enlaces rápidos

## Tecnologías

- **Vue 3** (Composition API)
- **Vite** (Build tool)
- **Vue Router** (Navegación)
- **TailwindCSS** (Estilos)
- **Google Fonts** (Tipografía: Playfair Display + Inter)

## Instalación

1. Clonar el repositorio
2. Instalar dependencias:
```bash
npm install
```

## Desarrollo

Para iniciar el servidor de desarrollo:
```bash
npm run dev
```

El servidor se ejecutará en `http://localhost:3000`

## Producción

Para construir el proyecto para producción:
```bash
npm run build
```

Para previsualizar la build de producción:
```bash
npm run preview
```

## Estructura del Proyecto

```
src/
|-- assets/          # Imágenes y recursos estáticos
|-- components/      # Componentes Vue
|   |-- Navbar.vue
|   |-- Hero.vue
|   |-- Productos.vue
|   |-- Historia.vue
|   |-- Horarios.vue
|   |-- Contacto.vue
|   |-- Footer.vue
|-- router/          # Configuración de Vue Router
|-- styles/          # Estilos globales y Tailwind
|-- views/           # Páginas principales
|   |-- Home.vue
|-- App.vue          # Componente raíz
|-- main.js          # Punto de entrada
```

## Personalización

### Colores
Los colores principales están definidos en `tailwind.config.js`:
- `verde-oscuro`: #1a3d2e
- `dorado`: #d4af37
- `crema`: #faf8f3

### Componentes
Cada componente es modular y puede ser personalizado fácilmente. Los estilos están organizados con:
- Estilos globales en `src/styles/main.css`
- Estilos específicos en cada componente (scoped)
- Clases utilitarias de TailwindCSS

## SEO

El sitio incluye optimización SEO básica:
- Meta tags descriptivos
- Open Graph tags
- Estructura semántica HTML5
- Tipografías web optimizadas
- Imágenes con alt attributes

## Deploy

El proyecto está listo para ser desplegado en cualquier plataforma estática como:
- Vercel
- Netlify
- GitHub Pages
- Firebase Hosting

## Licencia

Proyecto desarrollado para Les Délices - Todos los derechos reservados.