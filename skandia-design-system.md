---
name: skandia-design-system
description: >
  Guía técnica del Design System de Skandia (Skandia UI Kit v0.1.0) para generar código frontend
  fiel a la marca. Usa esta habilidad SIEMPRE que el usuario pida construir, revisar o modificar
  componentes de UI para Skandia — botones, formularios, tarjetas, layouts, dashboards, pantallas
  de app, simuladores o cualquier interfaz digital — o cuando mencione tokens de color, componentes
  del DS, Figma Skandia, PrimeNG con estilos Skandia, o cualquier tarea de frontend que deba verse
  y sentirse como Skandia. Actívala también cuando el usuario use palabras como "componente Skandia",
  "UI Skandia", "DS Skandia", "diseño Skandia", "pantalla para la app", "simulador tributario",
  o cuando pida código Angular/React/CSS/HTML para productos digitales de Skandia. Esta habilidad
  complementa skandia-brandbook (identidad visual) y skandia-comunicacion (voz y tono) —
  úsalas en conjunto cuando el entregable sea una pieza completa de UI con copy.
---

# Skandia Design System — Guía de Implementación
`Skandia UI Kit v0.1.0 · Stack: Angular + TypeScript + CSS Variables + PrimeNG`

> **Regla de oro:** Nunca inventar tokens, variantes ni tamaños. Todo lo que no esté documentado aquí debe consultarse con el equipo UX. Contacto: uxcolombia@skandia.com.co

---

## 🧭 Identidad del Sistema

| Propiedad | Valor |
|---|---|
| Nombre | `Skandia UI Kit` |
| Versión | `0.1.0` |
| Unidad base de espaciado | `8px` |
| Modo de color activo | `Light` |
| Stack | **Angular + TypeScript + CSS Variables** |
| Librería de componentes | **PrimeNG** |
| Librería de íconos | **Font Awesome 6 Free** |
| Fuente Figma | `rlrjl6jIlMtNR0o3EVH1jB` |

### Instalación

```bash
npm install primeng @primeng/themes primeicons
npm install @fortawesome/fontawesome-free
```

En `styles.scss` global:
```scss
@import '@fortawesome/fontawesome-free/css/all.min.css';
```

---

## 🎨 Tokens de Color

**Regla absoluta: Nunca hardcodear colores. Siempre `var(--color-*)`.**

Ver declaración `:root` completa en `references/tokens.md` → Sección 1.

**Tokens semánticos de uso frecuente:**

| Contexto | Token |
|---|---|
| Texto principal (H1, body) | `--color-text-body-heading-1` |
| Texto secundario / labels | `--color-text-body-heading-2` |
| Titulares con acento de marca | `--color-text-heading` |
| Links | `--color-text-link` |
| Fondo página | `--color-bg-main` |
| Fondo secciones alternas | `--color-bg-grey-light` |
| Fondo cards con énfasis de marca | `--color-bg-brand-light` |
| Bordes de campos | `--color-stroke-grey-light` |
| Bordes activos / foco | `--color-stroke-brand` |
| Error | `--color-feedback-error-dark` |
| Éxito | `--color-feedback-success-dark` |
| Advertencia | `--color-feedback-warning-dark` |
| Información | `--color-feedback-info-dark` |
| Botón primario | `--color-button-primary-default` |
| Botón hover | `--color-button-primary-hover` |

**Reglas críticas:**
- `--color-primary-green-00` (`#00C73D`) es el color brand principal — CTAs, acciones primarias, estados activos.
- Tonos `d01–d04`: hover/pressed. Tonos `l01–l05`: fondos, disabled.
- Nunca usar teal o secondary-green como color de acción primaria.
- Colores secundarios no deben exceder el **33%** del área total del color principal.

---

## 🔤 Tipografía

| Rol | Fuente | Uso |
|---|---|---|
| **Títulos** | **Montserrat** | H1–H6, labels de botón |
| **Cuerpo** | **Open Sans** | Body, campos, tooltips |
| **Valores numéricos** | **Monoespaciada** (IBM Plex Mono) | Cifras monetarias en tablas |

```html
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&family=Open+Sans:wght@400;500;700&display=swap" rel="stylesheet">
```

**Estilos clave (escala completa en `references/tokens.md` → Sección 2):**

| Estilo | Fuente | Peso | Tamaño | Uso |
|---|---|---|---|---|
| `pageTitleH1Bold` | Montserrat | 700 | 32px | Titular principal |
| `sectionTitleH2Bold` | Montserrat | 700 | 24px | Métricas destacadas |
| `subsectionTitleH3Medium` | Montserrat | 500 | 20px | Títulos de sección |
| `metaTitleH5Medium` | Montserrat | 500 | 16px | Labels de campos |
| `bodyMedium` | Open Sans | 500 | 16px | Texto de interfaz estándar |
| `labelBold` | Open Sans | 700 | 14px | Texto de botón primario |
| `captionBody3` | Open Sans | 500 | 12px | Textos de ayuda, referencias |

**Reglas:** Botones en `labelBold`. Nunca italic en botones. Texto disabled con `opacity: 0.4`. Cifras monetarias en monoespaciada.

---

## 📐 Espaciado y Grilla

Unidad base: **8px**. Todos los espaciados deben ser múltiplos de 8.

| Token | Valor | Uso típico |
|---|---|---|
| `--space-1` | 8px | Gap ícono-texto |
| `--space-2` | 16px | Padding interno de campos |
| `--space-3` | 24px | Separación entre campos |
| `--space-4` | 32px | Separación entre secciones |
| `--space-5` | 40px | Margen entre bloques de resultados |
| `--space-6` | 48px | Padding de contenedores principales |

**Grilla responsive:**

| Breakpoint | Columnas | Gutter | Margen |
|---|---|---|---|
| Mobile (< 768px) | 4 | 16px | 16px |
| Tablet (768–1024px) | 8 | 24px | 24px |
| Desktop (> 1024px) | 12 | 24px | 48px |

Usar grilla PrimeNG: `p-fluid`, `p-grid`, `p-col-*`. **Ancho máximo de contenido: 800px.**

---

## 🔘 Componentes

> **Regla crítica PrimeNG:** Nunca usar estilos default de PrimeNG sin aplicar tokens Skandia.

### Button — Completamente documentado en v0.1.0

Ver spec completa en `references/button.md`.

**Reglas críticas:**
- Máximo **1 botón Primary** por vista.
- Jerarquía: Primary → Secondary → Tertiary.
- Texto siempre en **verbo infinitivo**: "Iniciar simulación", "Confirmar y enviar".
- Alturas fijas: Small = `30px`, Large = `48px`. **Nunca cambiarlas.**
- Mobile CTAs principales: `fullWidth`.
- `icon-only` siempre requiere `aria-label`.

### Componentes PrimeNG con tokens Skandia

Ver especificaciones completas en `references/components-primeng.md`.

| Componente | PrimeNG | Spec clave Skandia |
|---|---|---|
| **InputText** | `p-inputtext` | Altura 48px, focus: `2px solid --color-stroke-brand`, label fija encima |
| **InputSwitch** | `p-inputswitch` | Track activo `--color-primary-green-00`, 44×24px, siempre con label visible |
| **Card** | `p-card` | `border-radius: 12px`, padding 24px. Variantes: Default / Brand Light / Metric |
| **Tooltip** | `pTooltip` | Ícono `fa-circle-question` verde, máx 280px, `role="tooltip"` |
| **Dialog** | `p-dialog` | Máx 480px, `border-radius: 16px`, botón cierre `fa-xmark` |
| **Steps** | `p-steps` | Activo: relleno verde. Completado: `fa-check`. Pendiente: borde gris |
| **DataTable** | `p-table` | Header `--color-bg-grey-light`, monoespaciada alineada derecha, sticky header |
| **Chart** | `p-chart` | Barras dobles: actual `#8ba2c1` / óptima `#00c73d`, leyenda `bottom` |
| **Badge/Chip** | `p-badge`, `p-chip` | 4 variantes: éxito / calculado / advertencia / info |
| **Toast** | `p-toast` | `top-right`, 4000ms, íconos Font Awesome por tipo |

---

## 🎨 Iconografía — Font Awesome 6

**Solo Font Awesome 6 Free. No mezclar con PrimeIcons u otras librerías.**

Usar `fa-regular` por defecto. Reservar `fa-solid` para estados activos.

**Íconos clave por contexto:**

| Contexto | Clase CSS | Color |
|---|---|---|
| Tooltip / ayuda | `fa-regular fa-circle-question` | `--color-primary-green-00` |
| Validación exitosa | `fa-solid fa-circle-check` | `--color-feedback-success-dark` |
| Error | `fa-solid fa-circle-exclamation` | `--color-feedback-error-dark` |
| Advertencia | `fa-solid fa-triangle-exclamation` | `--color-feedback-warning-dark` |
| Aporte óptimo | `fa-solid fa-piggy-bank` | `--color-primary-green-00` |
| Contacto asesor | `fa-solid fa-user-tie` | `--color-icon-dark` |
| Correo | `fa-regular fa-envelope` | `--color-icon-dark` |
| Colapsar/expandir | `fa-solid fa-chevron-up/down` | `--color-icon-medium` |
| Paso completado | `fa-solid fa-check` | `--color-neutral-00` |
| Privacidad | `fa-solid fa-shield-check` | `--color-primary-green-00` |
| Cierre modal | `fa-solid fa-xmark` | `--color-icon-dark` |

**Reglas:**
- Íconos nunca comunican información de forma exclusiva — siempre acompañan texto o tienen `aria-label`.
- Tamaño base: `16px`. Métricas/CTAs: `20px`–`24px`.
- Decorativos: `aria-hidden="true"`. Interactivos sin texto: `aria-label` + `tabindex="0"` + `role="button"`.

---

## 🎞️ Animaciones

Ver tokens y keyframes completos en `references/animations.md`.

**Principios:**
- Duración: 150ms–350ms. **Nunca superar 400ms.**
- Siempre respetar `prefers-reduced-motion: reduce`.
- Las animaciones nunca bloquean la interacción.

**Animaciones implementadas:**

| Nombre | Uso |
|---|---|
| `[@fieldReveal]` | Aparición/desaparición de campos condicionales al activar toggles |
| `ska-metric-value--updated` | Micro-pulso verde en valores que se recalculan |
| `[@pageTransition]` | Transición entre pantallas (entra desde derecha al avanzar, izquierda al retroceder) |
| `ska-card-optimal--appear` | Highlight de atención en card de aporte óptimo al aparecer en resultados |
| `ska-btn-spinner` | Spinner inline en botón primary durante estado de carga |
| `.ska-chevron--open` | Rotación 180° del chevron al colapsar/expandir secciones |

---

## ♿ Accesibilidad

Estándar mínimo: **WCAG 2.1 AA.**

- Texto normal: ratio contraste mínimo **4.5:1**.
- Texto grande (18px+ o 14px+ bold): ratio mínimo **3:1**.
- Nunca comunicar información solo mediante color.
- Todo elemento interactivo accesible por `Tab`, `Enter`, `Space`, flechas.
- Estado `:focus` siempre visible — **nunca** `outline: none` sin reemplazo.
- Formularios Angular con `ReactiveFormsModule`: `<label [for]>`, `aria-describedby` en errores, `aria-required="true"`.
- Tablas: `<thead>`, `<th scope="col">` en todas las columnas.

---

## 🗣️ Voz y Tono (resumen)

Ver guía completa en skill `skandia-comunicacion`.

- Siempre **"tú"**. Nunca "usted" ni impersonal.
- Verbos **permitidos:** `Puedes · Conoce · Aquí verás · Evalúa · Revisa · Explora`
- Verbos **prohibidos:** `Te recomendamos · Deberías · Te conviene · Debes · Tienes que`
- Errores que guían: "Este dato es necesario para calcular tu retención." — nunca "Campo requerido."

---

## 🖼️ Logo y Marca

- Versión principal: sobre fondo blanco o claro. Versión blanco total: sobre fondo verde.
- Tamaño mínimo digital: **200px de ancho**.
- ❌ Nunca estirar, recolorear, rotar (solo 0°, 45°, 90°), ni aplicar efectos.

---

## 📏 Reglas Globales de Código

### ✅ Siempre
- CSS variables en `:root`. `var(--color-*)` para todos los colores.
- Estados: hover, focus, pressed, disabled.
- `aria-label` en elementos interactivos sin texto visible.
- `:focus` visible obligatorio.
- Nombres exactos de Figma: `Primary`, `Secondary`, `Tertiary`, `Small`, `Large`.

### ❌ Nunca
- Hardcodear colores. Inventar tokens. Crear variantes no documentadas sin consultar.
- Cambiar alturas de botones. Usar estilos default de PrimeNG sin tokens Skandia.
- Usar teal o secondary-green en acciones primarias.

### 🧠 Flujo de generación de código
1. Leer esta skill + references necesarias.
2. Declarar todas las CSS variables en `:root`.
3. Usar solo tokens y componentes documentados.
4. Si el componente no está documentado → consultar antes de crearlo.
5. Revisar accesibilidad: aria-labels, focus ring, contraste.
6. Stack: **Angular + TypeScript + CSS Variables** salvo que el usuario especifique otro.

---

## 📂 Referencias

| Archivo | Contenido | Cuándo leer |
|---|---|---|
| `references/tokens.md` | Declaración `:root` completa (color, tipografía, espaciado) | Siempre que necesites tokens específicos |
| `references/button.md` | Spec completa del Button: CSS variables, estados, código Angular | Al implementar cualquier botón |
| `references/components-primeng.md` | Spec de los 10 componentes PrimeNG con tokens Skandia | Al implementar formularios, tablas, cards, charts, modales |
| `references/animations.md` | Tokens de animación, keyframes, Angular Animations completos | Al implementar transiciones o micro-interacciones |
