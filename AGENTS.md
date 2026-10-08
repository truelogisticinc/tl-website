# AGENTS.md - Instrucciones para Agentes de IA

Este archivo contiene información específica para que los agentes de IA entiendan el proyecto y continúen el trabajo eficientemente.

## 📋 INFORMACIÓN DEL PROYECTO

**Nombre:** True Logistic Website
**Tipo:** Sitio web estático para empresa de distribución de mariscos
**Ubicación:** Miami, Florida, Estados Unidos
**Cliente:** True Logistic Investments, Inc. - Distribuidor mayorista de mariscos a nivel regional y nacional

**Contexto del Negocio:**
- Distribuidor mayorista de mariscos (wholesale-to-wholesale)
- Ubicado en Miami, FL con centro de distribución refrigerado/congelado
- Compra pescado fresco de alta calidad de todo el mundo (incluyendo Golfo de México)
- Cumple con regulaciones FDA
- Servicio 24/7/365
- Distribución nacional
- Clientes: restaurantes, distribuidores, cadenas de restaurantes

**Estilo y Branding:**
- Colores principales: Azul (#0066cc, #0099ff) - representa confianza, frescura, mar
- Colores secundarios: Amarillo (#EEF900) - representa energía, calidad
- Tipografía: Poppins (moderna, profesional)
- Estilo: Profesional, fresco, confiable, premium
- Público objetivo: B2B (restaurantes, distribuidores)

## 🔄 FLUJO DE TRABAJO CON GIT

**Flujo SIMPLIFICADO (NO usar Git Flow completo):**
```
feature → develop → main (con tag) → develop (back merge)
```

**Pasos específicos:**
1. Crear feature desde develop: `git checkout -b feature/nombre-feature develop`
2. Hacer cambios y commits
3. Push y crear PR: feature → develop
4. Merge a develop (en GitHub)
5. Cuando esté listo para release:
   - `git checkout main`
   - `git merge develop`
   - `git tag -a v1.0.0 -m "Release v1.0.0"`
   - `git push origin main`
   - `git push origin v1.0.0`
6. Sincronizar develop con main:
   - `git checkout develop`
   - `git merge main`
   - `git push origin develop`

**Decisiones tomadas:**
- NO usar ramas release (flujo simplificado para proyecto pequeño)
- Usar tags para versionamiento (v1.0.0, v1.1.0, etc.)
- Usar ramas backup solo para cambios temporales/riesgosos
- Semantic Versioning: MAJOR.MINOR.PATCH

**Estado actual:**
- main tiene tag v1.0.1
- develop está sincronizado con main
- Rama release/1.0.1 ya no se usa (puede borrarse)

## 📝 MEJORAS PENDIENTES

### 1. ARQUITECTURA Y ESTRUCTURA
**Estado:** Pendiente
**Prioridad:** Media
**Cambios propuestos:**
- Reorganizar estructura de archivos CSS
- Separar CSS en: variables, reset, base, components, layout, sections
- Modularizar JavaScript con POO
- Crear sistema de componentes reutilizables

### 2. ESTILO Y DISEÑO (CSS)
**Estado:** Pendiente
**Prioridad:** Alta (cambios visuales inmediatos)
**Cambios propuestos:**
- Implementar sistema de CSS variables (Design System)
- Colores: Paleta basada en azul (mar) y amarillo (energía)
- Tipografía: Poppins + Inter (para mejor legibilidad)
- Espaciado: Escala de 8px
- Border radius, shadows, transitions consistentes
- Optimizar fuentes con font-display: swap
- Usar CSS Grid para layouts complejos
- Eliminar !important (actualmente 3 usos)

**Sistema de colores propuesto:**
```css
--color-primary: #0066cc;      /* Azul principal */
--color-primary-light: #0099ff; /* Azul claro */
--color-primary-dark: #004d99;  /* Azul oscuro */
--color-secondary: #EEF900;    /* Amarillo */
--color-text-primary: #1a365d; /* Texto principal */
--color-text-secondary: #4a5568; /* Texto secundario */
```

### 3. JAVASCRIPT Y MODERNIZACIÓN
**Estado:** Pendiente
**Prioridad:** Media
**Cambios propuestos:**
- Modularizar JavaScript con POO
- Separar concerns: config, utils, components
- Eliminar código duplicado (AOS.init está en HTML y JS)
- Agregar manejo de errores
- Validación de formularios de contacto
- Usar JSDoc para type checking

**Estructura propuesta:**
```
assets/js/
├── config.js
├── utils/
│   ├── helpers.js
│   └── validators.js
├── components/
│   ├── Navbar.js
│   ├── ProductCard.js
│   └── ContactForm.js
└── main.js
```

### 4. HTML Y SEMÁNTICA
**Estado:** Pendiente
**Prioridad:** Alta
**Cambios propuestos:**
- Corregir gramática en inglés (currently has poor grammar in testimonials)
- Consistencia de idioma (actualmente mezcla inglés/español)
- Sección de contacto está en español, resto en inglés
- Corregir "How makes us different?" → "What makes us different?"
- Corregir link de Bootstrap (línea 14: rel="stylesheet" duplicado)
- Corregir botón "Products" que redirige a #servicios (debería ser #products)
- Agregar aria-label para accesibilidad
- Agregar Open Graph tags para redes sociales
- Agregar schema.org structured data
- Validar con W3C validator

**Textos a corregir (gramática):**
- Testimonial 1: "They provide confidence and security, my company chooses them for you" → Improve grammar
- Testimonial 2: "Since working with you I have received really fresh fish" → Improve grammar
- Testimonial 3: "We like his grading and when I have not been able withdraw my product" → Improve grammar

### 5. PERFORMANCE Y SEO
**Estado:** Pendiente
**Prioridad:** Media
**Cambios propuestos:**
- Lazy loading para imágenes (`loading="lazy"`)
- Preload para fuentes críticas
- Comprimir imágenes (WebP format)
- Minificar HTML, CSS, JS
- Agregar rel="preconnect" para CDNs
- Agregar sitemap.xml
- Agregar robots.txt
- Implementar Service Worker para PWA

### 6. TESTING Y QA
**Estado:** Pendiente
**Prioridad:** Baja
**Cambios propuestos:**
- Tests unitarios con Jest (para JS)
- Tests visuales con Playwright
- Lighthouse CI para performance
- Validación de HTML con HTML-validate
- Validación de accesibilidad con axe

### 7. DOCUMENTACIÓN
**Estado:** En progreso (este archivo)
**Prioridad:** Alta
**Cambios propuestos:**
- README.md completo con instrucciones
- Comentarios JSDoc en JavaScript
- Documentación de componentes

## 🛠️ HERRAMIENTAS Y CONFIGURACIÓN

**Dependencias actuales:**
- Bootstrap 5.3.8 (CDN)
- AOS 2.3.4 (Animate On Scroll)
- Font Awesome 6.4.0
- Google Fonts (Poppins)

**Herramientas recomendadas (futuras):**
- ESLint para JavaScript
- Stylelint para CSS
- Prettier para formatting
- Vite o Webpack para bundling
- PostCSS para procesar CSS

**No usar:**
- PEP8 (es para Python, no aplica aquí)
- Linters de Python

## 📊 ORDEN RECOMENDADO DE MEJORAS

**Opción A (Resultados rápidos primero):**
1. Estilo (CSS variables, colores, tipografía)
2. Gramática y consistencia de idioma
3. HTML semántico y SEO
4. JavaScript modularizado
5. Arquitectura completa

**Opción B (Base sólida primero):**
1. Arquitectura y estructura de archivos
2. Sistema de diseño (CSS variables)
3. Estilo y tipografía
4. JavaScript POO
5. Gramática y SEO

## ⚠️ REGLAS IMPORTANTES

**Para el agente:**
1. Siempre mostrar diff de cambios antes de git commit
2. Esperar aprobación explícita del usuario antes de commitear
3. Nunca hacer git push sin aprobación del usuario
4. Probar cambios en navegador antes de commitear
5. Usar flujo de Git simple (feature → develop → main)
6. Respetar el contexto del negocio (distribuidora de mariscos en USA)
7. Usar colores y estilos apropiados para el sector (azul/mar, profesional)

**Para el usuario:**
1. Revisar cambios en navegador (http://localhost:8000) antes de aprobar
2. Usar DevTools para probar responsive (F12 → modo dispositivo)
3. Crear backup antes de cambios grandes: `git branch backup`
4. Usar tags para versiones, no ramas backup
5. Revisar pull requests en GitHub antes de merge

## 🎯 PRÓXIMOS PASOS INMEDIATOS

1. Implementar sistema de CSS variables (cambios visuales inmediatos)
2. Corregir gramática y consistencia de idioma
3. Optimizar estructura CSS
4. Modularizar JavaScript
5. Agregar validación de formulario de contacto

## 📞 CONTACTO DEL PROYECTO

**Desarrollador:** LKS Engineer
**GitHub:** https://github.com/lksengineer
**Repositorio:** https://github.com/truelogisticinc/tl-website

**Información de contacto de la empresa:**
- Dirección: 8321 Nw 90th St Medley, FL 33166
- Teléfono: +1(813)4559132
- Email: ar@truelogisticinc.com
- Contacto: Ramón Turmero

## 🔄 HISTORIAL DE DECISIONES

**Sesión actual (2026-10-08):**
- Decidido usar flujo simplificado de Git (sin ramas release)
- main tiene tag v1.0.1
- develop está sincronizado con main
- Creados archivos de documentación AGENTS.md y PROJECT_CONTEXT.md
- Decidido empezar con mejoras de estilo (CSS variables) para resultados visuales rápidos

## 📝 NOTAS ADICIONALES

- El proyecto usa Firebase Hosting para despliegue
- Imágenes están en public/assets/img/
- CSS está en public/assets/css/ (styles.css, products.css)
- JavaScript está en public/assets/js/main.js
- El servidor local para desarrollo: `cd public && python3 -m http.server 8000`
- Preview en navegador: http://127.0.0.1:38011 (cuando está corriendo el servidor)
