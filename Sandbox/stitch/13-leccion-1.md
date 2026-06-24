# Pantalla 13 — Lección 1: ¿Para qué sirve ahorrar?
**ID:** leccion-1
**Canvas:** Mobile 375px
**Actor:** Adolescente
**Posición en el flujo:** Accesible desde "Tu zona de aprendizaje" en el dashboard (P04)

---

## Prompt para Stitch

Diseña una pantalla de microlección financiera mobile (375px) para una adolescente de 16 años. No es una clase — es una experiencia breve, directa y con una pregunta al final. Tono: un coach que habla de igual a igual, no un profesor.

**Layout:** Scroll vertical. Header fijo. CTA fijo al fondo (aparece solo tras acertar la pregunta).

**Header fijo (fondo blanco, sombra sutil):**
- Flecha atrás (izquierda) que vuelve al dashboard
- Título centrado: "Nivel 1"
- Badge verde claro a la derecha: "En progreso"

**Barra de pasos (debajo del header, fija):**
- 4 círculos conectados por línea: paso 1 en verde relleno, pasos 2–3–4 en gris vacío
- Texto debajo: "Paso 1 de 4" en gris 12px

**Tarjeta de concepto (scroll, fondo blanco, `border-radius: 12px`, sombra suave):**
- Ilustración placeholder: rectángulo verde muy claro `#E8F8ED`, 100% ancho, 140px alto, ícono de alcancía verde 48px centrado
- Título H2 24px bold oscuro: "¿Para qué sirve ahorrar?"
- Cuerpo Open Sans 16px, interlineado 1.5:
  "Ahorrar no es solo guardar plata para no gastarla. Es separar una parte de lo que tienes ahora para lograr algo que quieres más adelante. Cada peso que guardas hoy es un paso hacia tu próxima meta."

**Pregunta de verificación (misma tarjeta, sección separada con línea divisoria):**
- Título 16px bold: "¿Cuál de estas es la mejor razón para ahorrar?"
- 3 opciones como radio-cards (borde gris 1px, `border-radius: 8px`, padding 14px):
  1. "Para no gastar todo de una vez"
  2. "Para lograr algo que quiero"
  3. "Porque mis papás me lo dijeron"
- Estado seleccionado: borde verde 2px + check verde a la derecha
- **Feedback correcto** (opción 2): caja verde claro `#E8F8ED`, ícono check verde, texto verde 14px: "¡Exacto! Ahorrar con propósito es más poderoso que ahorrar sin meta."
- **Feedback incorrecto** (opciones 1 y 3): caja gris `#F5F5F5`, texto gris 14px: "Casi — piénsalo de nuevo. ¿Cuál tiene más que ver con tus metas?"

**CTA fijo al fondo (aparece solo tras acierto):**
- Botón primario verde ancho completo: "Siguiente →"
- Al presionar: toast verde "Paso 1 completado · +10 puntos" y regresa al dashboard con barra de Nivel 1 actualizada a 25%

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Verde claro (feedback, ilustración): `#E8F8ED`
- Verde texto sobre claro: `#00703A`
- Fondo página: `#F5F5F5`
- Tarjeta: fondo blanco, `border-radius: 12px`, sombra `0 2px 8px rgba(0,0,0,0.08)`
- Cuerpo: Open Sans 16px, color `#333333`
- Barra de pasos: paso activo `#00C73D`, pasos pendientes `#D0D0D0`
- Toast: fondo verde, texto blanco, `border-radius: 8px`
- Sin emojis ni íconos infantiles
