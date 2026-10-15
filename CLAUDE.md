# Suite de Herramientas Ecuador (Herramientas EC)

Suite web de calculadoras y herramientas gratuitas, privadas y optimizadas para Ecuador.
Todo el procesamiento se ejecuta 100% en el navegador del cliente mediante JavaScript nativo (cero envío de datos a servidores, máxima privacidad y velocidad instantánea).

---

## 🛠️ Stack Tecnológico

- **Framework:** [Astro](https://astro.build) (Static Site Generation - SSG)
- **Despliegue:** Cloudflare Pages
- **Estilos:** Vanilla CSS con variables de diseño + Tailwind CSS v4
- **SEO & Datos Estructurados:** Schema.org (JSON-LD), OpenGraph, Sitemap XML (`@astrojs/sitemap`), Meta tags canónicos y FAQPage schemas
- **Monetización:** Placeholders preparados para Google AdSense (`AdPlaceholder.astro`)
- **Procesamiento:** 100% Client-Side JavaScript (sin backend, APIs externas ni recolección de datos)

---

## 🚀 Comandos de Desarrollo

```bash
# Iniciar servidor de desarrollo
npm run dev

# Compilar para producción (dist/)
npm run build

# Previsualizar build de producción
npm run preview
```

---

## 📁 Arquitectura del Proyecto

```text
/
├── public/
│   ├── favicon.ico / favicon.svg
│   └── robots.txt
├── src/
│   ├── components/
│   │   ├── Header.astro           # Barra de navegación superior
│   │   ├── Footer.astro           # Pie de página institucional y enlaces legales
│   │   ├── ToolCard.astro         # Tarjeta de herramienta para el grid principal
│   │   ├── AdPlaceholder.astro    # Ranuras de publicidad AdSense responsivas
│   │   └── FaqAccordion.astro     # Acordeón de preguntas frecuentes con animación
│   ├── layouts/
│   │   ├── BaseLayout.astro       # Layout raíz HTML con metatags, fonts y schema
│   │   └── ToolLayout.astro       # Layout estándar para páginas de herramientas
│   ├── pages/
│   │   ├── index.astro            # Portal principal y buscador de herramientas
│   │   ├── contacto.astro         # Formulario y datos de contacto
│   │   ├── politica-de-privacidad.astro # Política de privacidad estricta
│   │   ├── terminos-de-servicio.astro   # Términos legales de uso
│   │   ├── simulador-credito-ecuador.astro   # [Fase 2] Crédito, amortización Francés/Alemán
│   │   ├── calculadora-laboral-ecuador.astro # [Fase 3] Décimos, fondos IESS, finiquito
│   │   ├── calculadora-deficit-calorico.astro # [Fase 4] Macros y TMB
│   │   ├── compresor-imagenes.astro          # [Fase 5] Canvas WebP/PNG/JPG
│   │   └── formateador-json-limpiador-listas.astro # [Fase 6] JSON & listas
│   └── styles/
│       └── global.css             # Design tokens, variables CSS, componentes y estilos base
```

---

## 🗺️ Hoja de Ruta de Fases

| Fase | Herramienta / Módulo | Ruta | Estado |
| :--- | :--- | :--- | :--- |
| **Fase 1** | Andamiaje Astro, SEO, Layouts, Estilos Globales y Páginas Legales | `/`, `/contacto`, `/politica-de-privacidad`, `/terminos-de-servicio` | ✅ Completado |
| **Fase 2** | Simulador de Crédito Ecuador (Francés, Alemán, Tasas BCE, Exportación CSV) | `/simulador-credito-ecuador/` | ✅ Completado |
| **Fase 3** | Calculadora Laboral Ecuador (13°, 14°, Fondos IESS, Rol y Finiquito/Despido) | `/calculadora-laboral-ecuador/` | ✅ Completado |
| **Fase 4** | Calculadora de Calorías y Macros (Mifflin-St Jeor, TMB, Déficit/Superávit) | `/calculadora-deficit-calorico/` | ✅ Completado |
| **Fase 5** | Compresor y Convertidor de Imágenes (WebP/PNG/JPG client-side vía Canvas) | `/compresor-imagenes/` | ⏳ Pendiente |
| **Fase 6** | Formateador JSON y Limpiador de Listas (SQL IN(), deduplicador, parser) | `/formateador-json-limpiador-listas/` | ⏳ Pendiente |

---

## 📐 Pautas de Diseño y Experiencia de Usuario (UX/UI)

1. **Paleta de Colores y Modo Oscuro:**
   - Fondo: `#0f172a` (Slate 900)
   - Superficies de tarjetas: `#1e293b` (Slate 800)
   - Bordes: `#334155` (Slate 700)
   - Acento primario: `#10b981` (Emerald 500) y degradados esmeralda
   - Texto principal: `#f1f5f9`, Texto secundario: `#94a3b8`

2. **Componentes Clave por Herramienta:**
   - Hero descriptivo con icono, título e insignia de privacidad.
   - Formulario de entrada con validación en tiempo real.
   - Tarjetas KPI / Stat cards con valores calculados dinámicamente.
   - Visualización de desglose (barras o gráficos porcentuales).
   - Tabla interactiva de detalle o desglose mes a mes / rubro a rubro.
   - Botón de exportación (CSV o impresión) cuando aplique.
   - Artículo SEO extenso (`prose-dark`) explicando las normas legales (Código del Trabajo, BCE, IESS, etc.) con ejemplos prácticos.
   - Sección de preguntas frecuentes con `FaqAccordion` y marcado Schema.org `FAQPage`.
