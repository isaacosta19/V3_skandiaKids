# Ajustes V3 — Skandia Kids · El Método (para devolver a Claude design)

**Archivo objetivo:** `V3_Skandia Kids/Skandia Kids - El Método.dc.html` (revisado 2026-06-25)
**Uso:** pegar esta lista en la sesión de Claude design para pulir el prototipo. NO es rediseño; son correcciones puntuales.
**Decisiones del usuario (2026-06-25):** las insignias de P05 se mantienen (gamificación aceptada a propósito). La meta de ejemplo se unifica a "Concierto BTS".

---

## PROMPT (cópialo desde aquí)

```
Vamos a pulir el prototipo de "Skandia Kids — El Método" con ajustes puntuales.
NO rediseñes ni reorganices pantallas; solo corrige lo siguiente. Respeta el
design system Skandia que ya usas (verde #00c73d, Montserrat/Open Sans, sk-*).

PRIORIDAD 1 — cosas que hoy se ven rotas al navegar

1. ABRIDORES DE CONVERSACIÓN EN P07 (Detalle de plan) NO SE RENDERIZAN.
   Los datos existen (cada plan trae `abridores: [{label, quote}]`) y el wiring
   `planAbridores` / `planHasAbridores` ya está, pero el cuerpo del bucle está vacío.
   Renderiza, dentro del bloque "planHasAbridores", una tarjeta por cada abridor:
   - un encabezado pequeño "Según cómo sea tu hijo" arriba del grupo,
   - cada tarjeta muestra el {label} (ej. "Si es callado o le da pena el tema")
     como subtítulo y el {quote} como la frase abridora destacada (en tono cita).
   Verifica abriendo el plan recomendado "Abre la conversación sobre su futuro":
   sus 3 abridores deben aparecer.

2. UNIFICAR LA META DE EJEMPLO A "CONCIERTO BTS" EN TODAS LAS PANTALLAS.
   Hoy la tarjeta de Metas dice "Concierto BTS · $450.000 de $900.000 (55%)" pero
   el resto del prototipo todavía dice "Mis Air Force 1 · $99.000 de $180.000".
   Cámbialo a "Concierto BTS" (mismos montos $450.000 / $900.000, 55%) en:
   - el hub P05 (badge "1 meta activa · …"),
   - la billetera: selector de meta en "Hacer un aporte", pantalla "Aprobar
     solicitud" y el banner de solicitud,
   - el banner "Valentina te pidió un aporte" en la pantalla de Metas.
   Coherencia financiera: un concierto es corto plazo, así que asócialo a la
   "Cuenta de Ahorros ···4821", NO a "Fondo de Pensiones Voluntarias".
   Restaura también la tarjeta "Fondo universidad" en la lista de Metas (quedó
   vacía), con sus datos $1.200.000 / $24.000.000, para que cuadre con la billetera
   y con la feature de Universidad.

3. NOTA DE HONESTIDAD OBLIGATORIA EN P03 (Diagnóstico del hijo).
   Hoy el comentario "NOTA OBLIGATORIA" está vacío. Agrega, antes de los botones,
   un aviso visible (estilo nota suave, no error):
   "Esto es cómo VES a Valentina hoy. Más adelante, ella podrá contarnos su versión."

PRIORIDAD 2 — features que hoy son stubs (navegan a Planes)

4. PANTALLA REAL DE PLANEACIÓN UNIVERSITARIA (hoy la tarjeta va a goPlanes).
   Crea la pantalla: el detonante emocional. Campos de ejemplo (carrera, ciudad,
   costo estimado, horizonte en años) y una estrategia de ahorro sugerida, con CTA
   "Crear la meta universitaria" que lleve a crear meta. Tono adulto, sin promesas
   de rendimiento.

5. PANTALLA REAL DE CURSOS (hoy la tarjeta va a goPlanes).
   Crea la pantalla con los 2 cursos del Channel partidos por tema, marcados como
   opcionales ("para cuando quieras profundizar"). Nunca como puerta de entrada.

PRIORIDAD 3 — guardrails

6. MARCADORES "⚠️ Pendiente Legal/Ops".
   En la billetera (activar, aporte, aprobar solicitud) y en cualquier mención de
   producto Skandia, agrega una etiqueta discreta "⚠️ Pendiente Legal/Ops" para
   señalar que esos flujos no están validados. No prometas rendimientos.

PROCESO
- Muéstrame primero solo el PLAN de cómo aplicarás los 6 ajustes. No ejecutes
  hasta que lo apruebe.
- Mantén las insignias de P05 tal como están (decisión tomada).
- Si algo es ambiguo, pregúntame antes de asumir.
```

---

## Notas para ti (no van en el prompt)

- **Lo que NO entra:** las insignias de P05 (gamificación aceptada) y el motor
  generativo (sigue simulado a propósito en esta etapa).
- **El #1 (abridores) y el #2 (meta) son los que más se notan rotos** al hacer clic;
  por eso van de primero.
- Si Claude design propone convertir el arranque en wizard otra vez, corrígelo: el
  hub es híbrido, sin candados.
- Tras aplicar, vale la pena decidir si se archiva el html viejo de 7 etapas
  (`Skandia Kids - Metodo.dc.html`) para no confundir.
