# 📁 Estructura del Proyecto

```
la-vera-pasta/
├── 📄 index.html          # Archivo principal de la aplicación
├── 📄 manifest.json       # Manifest para PWA capabilities
├── 📄 robots.txt          # Configuración para bots de búsqueda
├── 📄 README.md           # Documentación principal
├── 📄 STRUCTURE.md        # Este archivo - estructura del proyecto
└── 📁 screenshots/        # Capturas de pantalla (opcional)
    ├── desktop.png
    ├── mobile.png
    └── cart.png
```

## 🧩 Componentes del Sistema

### 📄 `index.html` - Archivo Principal

#### Secciones HTML:
- **`<head>`** - Meta tags, SEO, favicon, estilos CSS
- **`<body>`** - Estructura principal de la aplicación
  - **Skip Link** - Accesibilidad para navegación por teclado
  - **Navegación Flotante** - Menú principal adaptativo
  - **Header Hero** - Sección de presentación principal
  - **Secciones de Menú** - Pastas, salsas, acompañamientos, etc.
  - **Carrito Flotante** - Sistema de compras
  - **Modal de Pedido** - Formulario de información del cliente
  - **Footer** - Información final y créditos

#### CSS Integrado:
- **Variables CSS** (`:root`) - Sistema de theming
- **Reset & Base** - Estilos fundamentales
- **Layout Components** - Grid, flexbox, containers
- **UI Components** - Botones, tarjetas, modales
- **Animations** - Keyframes y transiciones
- **Responsive Design** - Media queries
- **Accessibility** - Focus states, skip links

#### JavaScript Integrado:
- **Estado Global** - Gestión del carrito y configuración
- **Validaciones** - Regex patterns y validación en tiempo real
- **Persistencia** - localStorage con manejo de timestamps
- **Interacciones** - Event listeners y handlers
- **Accesibilidad** - Funciones para lectores de pantalla
- **Animaciones** - Intersection Observer API
- **WhatsApp Integration** - Generación de mensajes

## 🎨 Sistema de Diseño

### Colores Principales
```css
--primary-color: #d4671f    /* Naranja pasta italiana */
--primary-dark: #b8541a     /* Naranja oscuro */
--primary-light: #f4a460    /* Naranja claro */
--whatsapp-color: #25D366   /* Verde WhatsApp */
--text-color: #2c2c2c       /* Texto principal */
```

### Tipografía
- **Playfair Display** - Títulos y elementos decorativos
- **Inter** - Texto de contenido y UI

### Espaciado
- Sistema basado en `rem` y variables CSS
- Grid responsive con `minmax(320px, 1fr)`
- Padding y margin consistentes

## 🔧 Funcionalidades Principales

### 1. Sistema de Carrito
```javascript
// Estado del carrito
let cart = JSON.parse(localStorage.getItem('laverapastaCart')) || [];

// Funciones principales
- addToCart(itemId, itemName, price)
- updateQuantity(itemId, change)
- removeFromCart(itemId)
- saveCartToStorage()
- updateCartDisplay()
```

### 2. Validaciones
```javascript
// Patterns de validación
const validations = {
  phone: /^(\+56)?[0-9]{8,9}$/,
  name: /^[a-zA-ZáéíóúÁÉÍÓÚñÑ\s]{2,50}$/,
  time: /^([01]?[0-9]|2[0-3]):[0-5][0-9]$/
};

// Función de validación
validateField(input, validationType)
```

### 3. Accesibilidad
```javascript
// Anuncios para lectores de pantalla
announceToScreenReader(message)

// Trap focus en modales
trapFocus(element)

// Navegación por teclado
setupKeyboardNavigation()
```

### 4. Integración WhatsApp
```javascript
// Generación de mensaje
confirmOrder() {
  // Valida campos
  // Genera mensaje formatado
  // Abre WhatsApp
  // Limpia carrito
}
```

## 📱 Responsive Breakpoints

```css
/* Mobile First */
@media (max-width: 768px) {
  /* Estilos móviles */
}

/* Tablet y Desktop */
@media (min-width: 769px) {
  /* Estilos escritorio */
}

/* Preferencias de accesibilidad */
@media (prefers-reduced-motion: reduce) {
  /* Reduce animaciones */
}
```

## ♿ Características de Accesibilidad

### Elementos ARIA
- `role="main"`, `role="banner"`, `role="navigation"`
- `aria-label`, `aria-labelledby`, `aria-describedby`
- `aria-expanded`, `aria-pressed`, `aria-live`
- `aria-hidden` para elementos decorativos

### Navegación por Teclado
- **Tab** - Navegación secuencial
- **Enter/Space** - Activación de elementos
- **Escape** - Cerrar modales
- **Arrow keys** - Navegación en grupos

### Soporte para Lectores de Pantalla
- Estructura semántica HTML5
- Anuncios dinámicos con `aria-live`
- Descripciones contextuales
- Skip links mejorados

## 🔄 Flujo de Usuario

### 1. Entrada a la Página
```
Usuario llega → Hero Section → Scroll automático → Menú flotante aparece
```

### 2. Navegación del Menú
```
Ver productos → Leer descripción → Agregar al carrito → Ver controles cantidad
```

### 3. Proceso de Pedido
```
Abrir carrito → Revisar items → Proceder a WhatsApp → Llenar formulario → Confirmar → WhatsApp se abre
```

## 🛠️ Mantenimiento y Actualización

### Para Agregar Nuevos Productos:
1. Duplicar estructura HTML de un item existente
2. Cambiar IDs únicos y contenido
3. Verificar funcionalidad del carrito
4. Probar accesibilidad

### Para Modificar Estilos:
1. Usar variables CSS cuando sea posible
2. Mantener consistencia en spacing
3. Probar en múltiples dispositivos
4. Verificar contraste de colores

### Para Funcionalidades Nuevas:
1. Mantener accesibilidad como prioridad
2. Agregar validaciones apropiadas
3. Documentar nuevas funciones
4. Probar edge cases

## 📊 Métricas de Rendimiento

### Objetivos Lighthouse:
- **Performance**: 90+
- **Accessibility**: 100
- **Best Practices**: 90+
- **SEO**: 90+

### Core Web Vitals:
- **LCP** (Largest Contentful Paint): < 2.5s
- **FID** (First Input Delay): < 100ms
- **CLS** (Cumulative Layout Shift): < 0.1

## 🚀 Deployment

### Archivos Necesarios para Producción:
- ✅ `index.html` - Archivo principal
- ✅ `manifest.json` - PWA manifest
- ✅ `robots.txt` - SEO configuration
- ✅ `README.md` - Documentación

### Configuraciones Pre-Deploy:
1. Actualizar número de WhatsApp
2. Verificar meta tags y URLs
3. Optimizar imágenes (si las hay)
4. Validar HTML y CSS
5. Probar en múltiples navegadores

---

*Este documento describe la estructura completa del proyecto La Vera Pasta v1.0*
