# PROJECT_CONTEXT.md - Contexto del Proyecto True Logistic Website

## 📋 RESUMEN EJECUTIVO

**Proyecto:** Sitio web corporativo para True Logistic Investments, Inc.
**Tipo:** Sitio web estático (HTML/CSS/JavaScript)
**Industria:** Distribución mayorista de mariscos (seafood wholesale)
**Ubicación:** Miami, Florida, Estados Unidos
**Estado:** v1.0.1 lanzado en producción
**Próxima versión:** v1.1.0 (en desarrollo)

## 🎯 OBJETIVO DEL PROYECTO

Crear un sitio web profesional que:
- Muestre la información de la empresa (About Us)
- Destaque los servicios diferenciadores (What Makes Us Different)
- Presente el catálogo de productos (Products)
- Muestre testimonios de clientes (Testimonials)
- Proporcione información de contacto (Contact)
- Refleje profesionalismo, calidad y confianza

## 🏢 INFORMACIÓN DE LA EMPRESA

**Nombre:** True Logistic Investments, Inc.
**Industria:** Distribución mayorista de mariscos (wholesale-to-wholesale)
**Ubicación:** Miami, Florida, Estados Unidos
**Centro de distribución:** 8321 Nw 90th St Medley, FL 33166

**Servicios:**
- Distribución de mariscos frescos y congelados
- Servicio 24/7/365
- Almacenamiento refrigerado (FDA compliant)
- Entrega a domicilio
- Distribución nacional
- Calidad premium

**Productos principales:**
- Yellowfin Tuna (Fresh, Premium Grade)
- Bigeye Tuna (Fresh, Ultra Premium)
- Bluefin Tuna (Fresh, Luxury Grade)
- Mahi Mahi (Fresh, Premium Catch)
- Swordfish (Fresh, Gourmet Selection)
- Sea Bass (Fresh, Chef's Choice)

**Clientes:**
- Restaurantes
- Cadenas de restaurantes
- Distribuidores de alimentos
- Compradores mayoristas

## 🎨 DISEÑO Y BRANDING

### Identidad Visual
**Colores corporativos:**
- **Azul (#0066cc, #0099ff):** Representa el mar, confianza, profesionalismo
- **Amarillo (#EEF900):** Representa energía, calidad, frescura
- **Blanco/Gris:** Limpieza, modernidad

**Tipografía:**
- **Poppins:** Fuente principal (moderna, profesional)
- **Inter:** Fuente secundaria (para mejor legibilidad en texto largo)

**Estilo:**
- Profesional y confiable
- Fresco y moderno
- Premium (pero accesible)
- Limpio y organizado

### Público Objetivo
**B2B (Business to Business):**
- Gerentes de compras de restaurantes
- Directores de suministro de cadenas
- Distribuidores de alimentos
- Compradores mayoristas

**Características del público:**
- Buscan calidad y consistencia
- Valoran servicio confiable
- Necesitan proveedor confiable
- Toman decisiones basadas en confianza

## 🏗️ ARQUITECTURA TÉCNICA

### Tecnología
- **HTML5:** Estructura semántica
- **CSS3:** Estilos con Bootstrap 5
- **JavaScript:** Interactividad y animaciones
- **Bootstrap 5.3.8:** Framework CSS
- **AOS 2.3.4:** Animaciones al scroll
- **Font Awesome 6.4.0:** Iconos
- **Google Fonts:** Tipografía (Poppins)

### Estructura de Archivos
```
tl-website/
├── public/
│   ├── index.html (página principal)
│   ├── 404.html (página de error)
│   ├── assets/
│   │   ├── css/
│   │   │   ├── styles.css (estilos principales)
│   │   │   └── products.css (estilos de productos)
│   │   ├── js/
│   │   │   └── main.js (JavaScript principal)
│   │   └── img/ (imágenes)
│   └── vendor/ (librerías de terceros)
├── firebase.json (configuración Firebase)
├── .firebaserc (configuración Firebase)
└── README.md (documentación)
```

### Despliegue
- **Hosting:** Firebase Hosting
- **Dominio:** Configurado en Firebase
- **CI/CD:** Manual (actualmente)

## 🔄 FLUJO DE TRABAJO

### Desarrollo
1. Crear rama feature desde develop
2. Hacer cambios locales
3. Probar en servidor local: `cd public && python3 -m http.server 8000`
4. Commit y push a GitHub
5. Crear Pull Request: feature → develop
6. Code review y merge a develop

### Release
1. Cuando develop está listo
2. Merge develop → main
3. Crear tag (ej: v1.1.0)
4. Push a GitHub
5. Desplegar a Firebase Hosting

### Versionamiento
- **Formato:** Semantic Versioning (MAJOR.MINOR.PATCH)
- **Ejemplos:**
  - v1.0.0: Release inicial
  - v1.0.1: Bug fixes
  - v1.1.0: Nuevas features
  - v2.0.0: Breaking changes

## 📊 ESTADO ACTUAL

### Versiones
- **v1.0.1:** Versión actual en producción
- **develop:** Rama de desarrollo (sincronizada con main)

### Problemas Conocidos
1. **Gramática en inglés:** Testimonios tienen gramática pobre
2. **Idioma inconsistente:** Sección de contacto en español, resto en inglés
3. **Errores técnicos:**
   - Link de Bootstrap duplicado (rel="stylesheet" aparece 2 veces)
   - Botón "Products" redirige a #servicios (debería ser #products)
   - Título incorrecto: "How makes us different?" (debería ser "What makes us different?")
4. **Formulario de contacto:** No funcional (no tiene action ni method)
5. **JavaScript:** Código duplicado (AOS.init en HTML y JS)
6. **CSS:** Sin sistema de variables, valores hardcodeados

### Mejoras Pendientes
Ver AGENTS.md para lista completa de mejoras pendientes con prioridades.

## 🎯 OBJETIVOS FUTUROS

### Corto Plazo (v1.1.0)
- Implementar sistema de CSS variables
- Corregir gramática y consistencia de idioma
- Optimizar estructura CSS
- Modularizar JavaScript
- Agregar validación de formulario de contacto

### Mediano Plazo (v1.2.0)
- Implementar funcionalidad completa de formulario de contacto
- Optimizar performance (lazy loading, compresión de imágenes)
- Mejorar SEO (meta tags, sitemap, robots.txt)
- Agregar pruebas automatizadas

### Largo Plazo (v2.0.0)
- Refactorización completa de arquitectura
- Implementar PWA (Progressive Web App)
- Agregar CMS para gestión de contenido
- Integración con sistema de pedidos

## 📞 INFORMACIÓN DE CONTACTO

**Para desarrollo:**
- Desarrollador: LKS Engineer
- GitHub: https://github.com/lksengineer
- Repositorio: https://github.com/truelogisticinc/tl-website

**Para la empresa:**
- Dirección: 8321 Nw 90th St Medley, FL 33166
- Teléfono: +1(813)4559132
- Email: ar@truelogisticinc.com
- Contacto: Ramón Turmero

## 🔗 RECURSOS EXTERNOS

- **Bootstrap:** https://getbootstrap.com/
- **AOS:** https://michalsnik.github.io/aos/
- **Font Awesome:** https://fontawesome.com/
- **Google Fonts:** https://fonts.google.com/
- **Firebase Hosting:** https://firebase.google.com/docs/hosting

## 📝 NOTAS IMPORTANTES

- El sitio está en inglés (excepto sección de contacto que está en español - error)
- El público objetivo es B2B en Estados Unidos
- Los colores deben reflejar confianza (azul) y calidad/frescura (amarillo)
- El diseño debe ser profesional y moderno
- El sitio debe ser responsive (mobile-first)
- El SEO es importante para visibility en buscadores

## 🔄 HISTORIAL DE CAMBIOS

### v1.0.1 (2026-10-08)
- Release inicial
- Páginas principales: Home, About, What Makes Us, Products, Testimonials, Contact
- Implementado con Bootstrap 5
- Animaciones con AOS
- Responsive design

### v1.0.0 (Desarrollo)
- Estructura base del proyecto
- Configuración Firebase Hosting
- Primeras páginas HTML

## 🚀 PRÓXIMOS PASOS

1. Implementar sistema de CSS variables (Design System)
2. Corregir gramática y consistencia de idioma
3. Optimizar estructura de archivos CSS
4. Modularizar JavaScript con POO
5. Agregar validación de formulario de contacto
6. Optimizar performance y SEO

---

**Última actualización:** 2026-10-08
**Versión del documento:** 1.0
