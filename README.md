# MINAKAWA INVESTMENTS — Web

Landing page institucional con estética **industrial-futurista** para Minakawa Investments — servicios automotrices de alto estándar.

---

## Sistema de Diseño

### Paleta de colores

| Token CSS | Valor | Uso |
|---|---|---|
| `--bg-void` | `#0a0a0f` | Fondo base (negro carbón) |
| `--bg-dark` | `#0f1117` | Secciones principales |
| `--bg-panel` | `#14171f` | Sidebar, top-bar, footer |
| `--bg-card` | `#181c26` | Cards y paneles |
| `--cyan` | `#00f0ff` | Acento primario (neón/HUD) |
| `--amber` | `#ff9500` | Acento secundario (industrial) |
| `--text-primary` | `#e8ecf4` | Texto principal |
| `--text-secondary` | `#8892a4` | Texto de soporte |

### Tipografía

- **Títulos y UI**: `Orbitron` (Google Fonts) — geométrica, técnica, futurista.
- **Cuerpo**: `Space Grotesk` (Google Fonts) — legible, moderna, con carácter técnico.
- Encabezados en `uppercase` + `letter-spacing` amplio.

### Componentes clave

- **Botones** (`btn-primary`, `btn-outline`): esquinas chamfered vía `clip-path`, glow neón en hover.
- **Cards de servicio**: esquina biselada superior derecha con `clip-path`, indicador LED de estado.
- **Sidebar**: fixed con fondo de rejilla sutil, indicador de sistema activo pulsante.
- **Hero**: fondo de grid animado + efecto scanlines + glitch en el h1.
- **Stats bar**: contadores animados con Intersection Observer.
- **Globe ornamental**: anillos CSS animados para la sección de Importaciones.

### Efectos y animaciones

- Glitch en el hero headline (keyframes `glitch-a` / `glitch-b`).
- Contador numérico animado (`animateCounters`) disparado por scroll.
- Scroll-reveal via `IntersectionObserver` en cards.
- Reloj en tiempo real en la top-bar.
- Respeta `prefers-reduced-motion`: todas las animaciones se desactivan.

### Responsive

| Breakpoint | Comportamiento |
|---|---|
| `> 1200px` | Layout completo, sidebar fija |
| `900px – 1200px` | Sidebar fija, contacto en 1 columna |
| `< 900px` | Sidebar deslizante (hamburger toggle), grid simplificado |
| `< 600px` | Hero en columna, cards 1 col, botones full-width |

### Accesibilidad

- Contraste AA: texto primario (#e8ecf4) sobre fondos oscuros ≥ 7:1.
- `:focus-visible` en todos los elementos interactivos.
- `aria-*` en navegación, secciones y botón de menú.
- `role` y `aria-label` en regiones semánticas.
- `prefers-reduced-motion` deshabilita animaciones intensas.

---

## Stack

- HTML5 semántico · CSS3 (custom properties, clip-path, animations) · Vanilla JS
- Google Fonts: Orbitron + Space Grotesk
- Font Awesome 6 (iconos)
- Sin frameworks ni bundlers — desplegable directamente en GitHub Pages

## Despliegue

El sitio se publica automáticamente en GitHub Pages usando el `CNAME` configurado en el repositorio.

## Extender el diseño

1. **Nuevo color de acento**: cambiar `--cyan` y `--cyan-glow` en `:root`.
2. **Nueva sección**: copiar un bloque `<section class="content-section">` y seguir el patrón `section-label → section-title → section-line → contenido`.
3. **Nueva card**: copiar una `<article class="card">` y actualizar `card-id`, icono y texto.
4. **Nuevas páginas**: crear archivos `.html` adicionales enlazando el mismo `style.css`.
