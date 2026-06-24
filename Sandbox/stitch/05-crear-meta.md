# Pantalla 05 — Crear meta
**ID:** meta-crear
**Canvas:** Mobile 375px
**Actor:** Adolescente
**Posición en el flujo:** Flujo de creación de meta de ahorro

---

## Prompt para Stitch

Diseña una pantalla mobile (375px) donde una adolescente de 16 años crea una meta de ahorro en su app financiera. El formulario debe sentirse personal y rápido — no como un trámite bancario.

**Layout:** Pantalla en columna con scroll. Header con flecha "atrás". CTA fijo al fondo de la pantalla.

**Header:**
- Flecha de regreso a la izquierda
- Título de pantalla centrado (pequeño, 16px): "Nueva meta"

**Contenido:**
1. Título grande de pregunta: "¿Para qué quieres guardar?"
2. Campo de texto: sin label visible — solo placeholder grande: "Ej: mis tenis, viaje a Santa Marta, mi primer millón"
3. Campo de monto con label: "¿Cuánto necesitas?" — input numérico con prefijo "$" a la izquierda
4. Campo de fecha con label: "¿Para cuándo?" — selector de fecha
5. Checkbox con label: "Sin fecha por ahora"
6. Espacio visual entre el formulario y el CTA

**CTA fijo al fondo (safe area):**
- Botón primario ancho completo verde: "Crear esta meta"

**Estilo visual:**
- Campos con mucho espacio — no apretados
- El título-pregunta es el elemento principal, grande y directo
- Los campos son limpios: borde gris claro, sin exceso de decoración
- Al enfocar un campo, el borde se pone verde
- El prefijo "$" del campo de monto está en gris dentro del campo

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Campos de texto: altura 48px, borde `1px solid #D0D0D0`, `border-radius: 8px`, focus borde `2px solid #00C73D`
- Título pregunta: Montserrat Bold 26px
- Label campos: Open Sans Medium 14px, color gris oscuro
- Placeholder: gris claro, Open Sans Regular
- Checkbox: al activarse, check verde `#00C73D`
- Botón primario: fijo al fondo, verde `#00C73D`, blanco, altura 52px, `border-radius: 8px`
