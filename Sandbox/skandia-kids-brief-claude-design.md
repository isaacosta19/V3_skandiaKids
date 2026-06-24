# Brief paste-ready — Skandia Kids · El Método (para Claude design)
**Uso:** pegar en una sesión de Claude design/artifact para generar el prototipo navegable.
**Fuente de verdad:** `skandia-kids-PRD-metodo.md` (rev. 23 jun) — este brief es el resumen accionable.
**Caso de ejemplo vivo:** Andrés (padre, 50) · Valentina (hija, 16).

---

## PROMPT (cópialo desde aquí)

```
Actúa como design engineer senior. Construye un MVP funcional y navegable de
"Skandia Kids — El Método", la experiencia del PADRE dentro del portal web Skandia.

CONTEXTO EN 3 LÍNEAS
- Es un MÉTODO de crianza financiera para el padre, NO un curso ni una app para niños.
  El padre aprende a enseñarle a su hijo sobre plata, porque a él nadie le enseñó.
- Vive DENTRO del shell del portal web Skandia (desktop, header + menú lateral + contenido).
  No es un producto independiente.
- Tono Skandia ADULTO: serio, confiable, cálido. Acompañamiento, no gamificación.
  CERO estética infantil (eso es del hijo, y es otra fase).

EL ESPINAZO (3 movimientos)
  Arranque lineal corto:   Entrada → Diagnóstico del padre → Diagnóstico del hijo → TU RESULTADO (conciencia)
  Luego hub HÍBRIDO:       Home con un "coach" que recomienda 1 acción/semana + 4 features siempre visibles.
  REGLA CRÍTICA: el hub NO es un wizard de pasos. Las 4 features están todas accesibles
  y priorizadas; el coach recomienda y resalta, pero NUNCA bloquea. Donde el orden importa,
  pon "fricción suave" (un consejo en la tarjeta), no un candado.

LAS 11 PANTALLAS
  P01 Entrada — tarjeta en el home del portal + ítem en el menú lateral.
      Título: "Enséñale a tu hijo a manejar su plata." CTA: "Empezar".
  P02 Diagnóstico del padre — 4 preguntas (cómo se hablaba de dinero en su infancia /
      qué frase oía / su relación actual con el dinero / qué quiere que su hijo aprenda).
      Encuadre: "No hay respuestas buenas ni malas." Barra de avance corta.
  P03 Diagnóstico del hijo, RESPONDIDO POR EL PADRE — datos (nombre, edad) + 4 preguntas
      (relación con el dinero / qué hace al recibir plata / con qué frecuencia hablan /
      qué quiere enseñarle). NOTA OBLIGATORIA en pantalla: "Esto es cómo VES a [nombre].
      Más adelante, él/ella podrá contarnos su versión."
  P04 TU RESULTADO / LA CONCIENCIA — *** la pantalla clave ***. Texto personalizado de
      LONGITUD VARIABLE (en producción lo genera un LLM). Diséñala con el ejemplo de
      Andrés/Valentina ABAJO como contenido real, no con un placeholder corto.
      Debajo del texto: la acción recomendada de la semana + las 4 features ya desbloqueadas.
  P05 Home / dashboard del educador — HERO = la acción de la semana (lo más prominente).
      Debajo: las 4 features (tarjetas, priorizadas pero todas accesibles). Progreso del padre.
  P06 Feature PLANES — banco de experiencias segmentado por A QUIÉN SIRVE:
      "Para ti" / "Para tu hijo" / "En familia". La recomendada por el coach va destacada.
  P07 Detalle de un plan — objetivo + cómo hacerlo + 2-3 abridores de conversación según
      el carácter del hijo (el callado / el que pregunta / el desinteresado) + "registrar
      que lo hicimos" (fluyó / me costó / no se dio, sin castigo).
  P08 Feature METAS — crear meta (nombre, monto, fecha) asociada a un producto Skandia.
      Ej: "Mis Air Force 1 · $180.000" o "Fondo universidad de Valentina".
  P09 Billetera, cara del padre — activar + fondear (aporte directo o aprobar solicitud
      con PIN) + confirmación. Es el motor de Metas. (NO diseñar la vista del hijo.)
  P10 Feature PLANEACIÓN UNIVERSITARIA — el detonante emocional. Carrera, ciudad, costo
      estimado, horizonte, estrategia de ahorro. CTA a crear la meta universitaria.
  P11 Feature CURSOS — los 2 cursos del Channel partidos por tema, opcionales, "para
      cuando quieras profundizar". Nunca la puerta de entrada.

DATOS MOCK (consistentes en todas las pantallas)
  - Padre: Andrés, 50 años. Perfil que sale de su diagnóstico: creció oyendo "el dinero
    no alcanza" (escasez), hoy ordenado pero ansioso, teme transmitirle la angustia.
  - Hija: Valentina, 16 años. Gasta rápido lo que recibe; casi no hablan de dinero;
    la universidad está cerca.
  - Meta activa de ejemplo: "Mis Air Force 1" · objetivo $180.000 · va en $99.000 (55%).
  - Cuenta origen del padre: Cuenta de Ahorros Skandia ···4821.

TEXTO DE EJEMPLO PARA P04 (úsalo literal como contenido vivo de la conciencia):
  "Andrés, creciste oyendo 'el dinero no alcanza'. Eso te volvió cuidadoso, pero el
   silencio no protege a Valentina de esa sombra: se la transmite. Ella gasta rápido
   porque a los 16 aún no ha tenido que decidir nada importante con su plata — y te
   quedan unos 2 años antes de que se vaya a la universidad y la maneje sola. No tienes
   que volverte experto. Tienes que empezar a hablar."
  Acción recomendada (ejemplo): "Esta semana, 10 minutos: pregúntale qué quiere estudiar
   y dónde. Aún no es una charla de plata — es abrir la puerta."

REGLAS NO NEGOCIABLES
  - CERO pantallas del adolescente. El padre es el único actor en pantalla.
  - El hub es HÍBRIDO, no lineal: features visibles y sin candados, coach que prioriza.
  - NADA promete rendimientos ni resultados financieros. Avisos de producto/billetera
    van marcados como "⚠️ Pendiente Legal/Ops", no omitidos.
  - El campo de PIN existe pero puede ser placeholder; el botón se habilita al escribir.
  - Respeta ESTRICTAMENTE el design system Skandia que ya conoces (componentes sk-*,
    paleta y tipografía oficiales). No inventes colores ni tipografías.

PROCESO
  - Primero muéstrame solo un PLAN por fases. No ejecutes hasta que lo apruebe.
  - Prioridad: 1) el arranque P01→P04→P05 (el corazón); 2) Planes P06-P07; 3) Metas+billetera
    P08-P09; 4) Universidad y Cursos P10-P11.
  - Entregable: .html autocontenido, desktop (viewport mínimo 1280px), simulando el shell
    del portal Skandia con la sección del método dentro.
  - Si algo es ambiguo, pregúntame antes de asumir.

Empieza mostrándome solo el PLAN.
```

---

## Recordatorios para ti (no van en el prompt)

- **Design system:** ya lo conoce, no tienes que pegarlo. Si ves que se desvía de la
  paleta/tipografía/componentes sk-*, recuérdaselo.
- **P04 es lo nuevo y frágil** — si el diseñador la hace con un placeholder de una línea, el layout se romperá cuando entre el texto largo del LLM. El ejemplo de Andrés/Valentina ya está en el prompt para evitarlo.
- **El riesgo recurrente es que vuelvan el hub en wizard** — el prompt lo advierte dos veces; si ves pasos numerados obligatorios en el plan, corrígelo de una.
- `content.md` NO va a esta sesión (está desactualizado). El microcopy esencial ya está aquí.
