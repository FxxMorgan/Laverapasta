# 🍝 La Vera Pasta

![Pasta Italiana](https://img.shields.io/badge/Pasta-Italiana-green?style=for-the-badge&logo=🍝)
![Made with Love](https://img.shields.io/badge/Made%20with-❤️-red?style=for-the-badge)
![Chile](https://img.shields.io/badge/Hecho%20en-Chile-blue?style=for-the-badge)

> **Auténtica pasta italiana hecha en casa** - Sistema de pedidos online profesional

## 🎯 Descripción

**La Vera Pasta** es una aplicación web moderna y completamente accesible para un restaurante de pasta italiana artesanal. Ofrece una experiencia de usuario excepcional con carrito de compras inteligente, validaciones en tiempo real, y integración directa con WhatsApp para pedidos.

### ✨ Características Principales

- 🛒 **Carrito de compras inteligente** con persistencia local
- 📱 **Integración WhatsApp** para pedidos directos
- ♿ **Completamente accesible** (WCAG 2.1 AA)
- 📱 **Responsive design** optimizado para móviles
- 🎨 **Interfaz moderna** con animaciones suaves
- 💾 **Persistencia de datos** con localStorage
- ✅ **Validaciones en tiempo real** con regex
- ⌨️ **Navegación completa por teclado**
- 🔍 **SEO optimizado** para mejor posicionamiento

## 🚀 Demo en Vivo

[Ver Demo](https://fxxmorgan.github.io/Laverapasta/) | [Capturas de Pantalla](#screenshots)

## 🛠️ Tecnologías Utilizadas

### Frontend
- **HTML5** - Estructura semántica y accesible
- **CSS3** - Variables personalizadas, Grid, Flexbox
- **JavaScript ES6+** - Funcionalidad moderna y robusta
- **Font Awesome 6** - Iconografía profesional
- **Google Fonts** - Tipografía Playfair Display e Inter
- **Anime.js** - Animaciones suaves y performantes

### Herramientas y Metodologías
- **Vanilla JavaScript** - Sin dependencias pesadas
- **CSS Custom Properties** - Theming consistente
- **Intersection Observer API** - Animaciones optimizadas
- **Local Storage API** - Persistencia de datos
- **Regex Validation** - Validaciones robustas
- **ARIA Standards** - Accesibilidad completa

## 📋 Funcionalidades Detalladas

### 🛒 Sistema de Carrito
- ✅ Agregar/remover productos con animaciones
- ✅ Control de cantidades intuitivo
- ✅ Persistencia automática en localStorage
- ✅ Limpieza automática de datos antiguos (1 hora)
- ✅ Contador dinámico de productos
- ✅ Cálculo automático de totales

### 📱 Integración WhatsApp
- ✅ Formulario de información del cliente
- ✅ Validación de campos en tiempo real
- ✅ Selección de hora de retiro
- ✅ Mensaje formateado automáticamente
- ✅ Apertura directa en WhatsApp

### ♿ Accesibilidad
- ✅ Navegación completa por teclado
- ✅ Soporte para lectores de pantalla
- ✅ Elementos ARIA completos
- ✅ Skip links mejorados
- ✅ Focus trap en modales
- ✅ Anuncios dinámicos para usuarios con discapacidades visuales

### 📱 Responsive Design
- ✅ Mobile-first approach
- ✅ Menú hamburguesa en móviles
- ✅ Carrito optimizado para pantallas pequeñas
- ✅ Touch-friendly interfaces
- ✅ Imágenes y texto adaptables

## 🏃‍♂️ Instalación y Uso

### Requisitos Previos
- Navegador web moderno (Chrome 90+, Firefox 88+, Safari 14+)
- Servidor web local (opcional para desarrollo)

### Instalación Rápida

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/la-vera-pasta.git
   cd la-vera-pasta
   ```

2. **Abrir en navegador**
   ```bash
   # Opción 1: Abrir directamente
   open index.html
   
   # Opción 2: Servidor local (Python)
   python -m http.server 8000
   
   # Opción 3: Servidor local (Node.js)
   npx serve .
   ```

3. **Personalizar configuración**
   - Editar número de WhatsApp en `index.html` (línea ~750)
   - Personalizar colores en variables CSS (líneas 15-35)
   - Modificar productos del menú según necesidades

## ⚙️ Configuración

### Número de WhatsApp
```javascript
// Cambiar en la función confirmOrder()
const whatsappUrl = `https://wa.me/56912345678?text=${encodeURIComponent(message)}`;
//                            ↑ Tu número aquí
```

### Variables de Colores
```css
:root {
  --primary-color: #d4671f;    /* Color principal */
  --primary-dark: #b8541a;     /* Color principal oscuro */
  --primary-light: #f4a460;    /* Color principal claro */
  --whatsapp-color: #25D366;   /* Color WhatsApp */
  /* ... más variables */
}
```

## 🎨 Capturas de Pantalla {#screenshots}

### Desktop
![Desktop View](screenshots/desktop.png)

### Mobile
![Mobile View](screenshots/mobile.png)

### Carrito de Compras
![Shopping Cart](screenshots/cart.png)

## 🧪 Testing

### Pruebas de Accesibilidad
- ✅ **WAVE** - Sin errores de accesibilidad
- ✅ **axe DevTools** - Cumple WCAG 2.1 AA
- ✅ **Lighthouse** - Puntuación 100% en accesibilidad
- ✅ **Navegación por teclado** - Completamente funcional

### Pruebas de Rendimiento
- ✅ **Lighthouse Performance** - 95+ puntos
- ✅ **Core Web Vitals** - Todas las métricas en verde
- ✅ **Mobile-friendly** - Test de Google aprobado

### Compatibilidad de Navegadores
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 🔧 Personalización

### Agregar Nuevos Productos
```html
<article class="menu-item" role="article" aria-labelledby="nuevo-producto" tabindex="0">
  <div class="menu-item-header">
    <div>
      <h3 class="menu-item-name" id="nuevo-producto">Nuevo Producto</h3>
      <p class="menu-item-description">Descripción del producto</p>
    </div>
    <div class="menu-item-price" aria-label="Precio: X pesos">$X.XXX</div>
  </div>
  <!-- ... resto del HTML -->
</article>
```

### Modificar Estilos
El proyecto usa variables CSS para fácil personalización:
```css
:root {
  --tu-variable: valor;
}
```

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Guías de Contribución
- Mantener la accesibilidad como prioridad
- Seguir las convenciones de código existentes
- Documentar nuevas funcionalidades
- Probar en múltiples navegadores

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👥 Créditos

### Desarrollado por
- **FxxMorgan** - *Desarrollo Full-Stack* - [@FxxMorgan](https://github.com/FxxMorgan)

### Recursos Utilizados
- [Font Awesome](https://fontawesome.com) - Iconografía
- [Google Fonts](https://fonts.google.com) - Tipografía
- [Anime.js](https://animejs.com) - Animaciones
- [Unsplash](https://unsplash.com) - Fotografías (si aplica)

## 📞 Contacto

**La Vera Pasta**
- 📧 Email: contacto@laverapasta.cl
- 📱 WhatsApp: [+56 9 78411973](https://wa.me/56978411973)
- 📍 Ubicación: Tomé, Chile
- 🌐 Website: [laverapasta.cl](https://laverapasta.cl)

---

<div align="center">

**¡Gracias por visitar La Vera Pasta!** 🍝

Si te gusta este proyecto, ¡dale una ⭐!

</div>

## 📊 Estadísticas del Proyecto

![GitHub stars](https://img.shields.io/github/stars/FxxMorgan/Laverapasta?style=social)
![GitHub forks](https://img.shields.io/github/forks/FxxMorgan/Laverapasta?style=social)
![GitHub issues](https://img.shields.io/github/issues/FxxMorgan/Laverapasta)
![GitHub last commit](https://img.shields.io/github/last-commit/FxxMorgan/Laverapasta)

## 🗺️ Roadmap

- [ ] 🌍 Internacionalización (i18n)
- [ ] 💳 Integración con MercadoLibre
- [ ] 📊 Dashboard de administración
- [ ] 🔔 Sistema de notificaciones
- [ ] 📱 Aplicación móvil nativa
- [ ] 🍕 Expansión a otros tipos de comida

---

<div align="center">
  <sub>Built with ❤️ by the La Vera Pasta team</sub>
</div>
