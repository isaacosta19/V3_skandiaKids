# PRD — Skandia Kids · El Método (Fase 1, centrado en el padre)
**Fecha:** 20 de junio de 2026 · **Rev. 23 de junio de 2026** — reescrito al nuevo espinazo (diagnóstico → conciencia → features)
**Estratega:** Skandia UX Team · #UXplorers
**Para:** Rachel (ux-ui-designer)
**Insumos:** skandia-kids-northstar.md ✅ (rev. 23 jun) · skandia-kids-research.md ✅ · skandia-kids-PRD.md → se reubica como **Fase 2** · producto_skandia_kids (MVP React) → **motor de la feature Metas**
**Nota de contenido:** ⚠️ Todo el microcopy es **provisional, pendiente de Kiki**. El resultado de conciencia y la acción de la semana son **generados por LLM** — aquí se define el marco, no el texto final.

> **Rev. 23 jun — qué cambió frente a la versión anterior:** el método deja de ser una **ruta lineal de 7 etapas** y pasa a **diagnóstico → conciencia → set de 4 features que el padre activa**. El diagnóstico se parte en dos (padre/hijo); el resultado se vuelve el hub de conciencia generado por LLM; el home pasa a ser un dashboard de features con un coach híbrido arriba; **desaparece la plantilla de etapa ×7**. Caso de ejemplo vivo: **Andrés (50) / Valentina (16)**.

---

## 1. Contexto

- **Caso:** Experimento de educación financiera familiar re-centrado en el **padre/cuidador** como protagonista. El producto es un **método de crianza financiera** que vuelve capaz al padre de enseñar. El hijo y la billetera (su visual) entran en la **Fase 2** (el PRD original).
- **Canal:** Vive **dentro del portal web Skandia existente** (sección dedicada), no es app ni producto independiente. El padre entra con sus credenciales actuales. La cadencia ("el método te busca") se resuelve por notificaciones del portal y/o correo — ver decisión pendiente.
- **Segmento principal — padre/cuidador:** *Family Guardian*. Educación financiera empírica: nunca recibió el método de sus propios padres. Muy motivado (1.281 se inscribieron solos al curso del Channel) pero el formato pasivo lo pierde (~9,4% lo termina). Detonante emocional: la universidad.
- **🚧 Alcance de diseño Fase 1 — la cara del padre:** La billetera **sí entra, pero solo desde el lado del padre** (activar, fondear, ver progreso — reúso de las pantallas parentales del PRD original / el MVP React). Lo que **NO se diseña en Fase 1 es la visual/interfaz del hijo** — ninguna pantalla del adolescente. Eso es Fase 2. **Nombre de trabajo:** "Skandia Kids" (marca pendiente; "Crecer Juntos" es título del método, no marca).
- **Outcome de negocio:** Demostrar que Skandia puede ser el **aliado de confianza en la crianza financiera de la familia** — convirtiendo padres motivados que el formato curso perdió en padres que sí enseñan, abriendo la puerta a la billetera del hijo (Fase 2) y a producto.
- **Problema del usuario (padre):** *"Quiere enseñarle a su hijo a manejar el dinero pero no tiene la herramienta ni el método."* La herramienta existe; el método no — y no lo tiene porque a él nunca se lo dieron.
- **Cómo medir el éxito:**
  - El padre completa **al menos una acción/conversación real** con su hijo (no "contenido visto"). Meta: batir por amplio margen el baseline del **9,4%**.
  - Cadencia sostenida: el padre vuelve, no abre-una-vez.
  - **Activación de features:** cuántas de las 4 toca y en qué orden (valida el modelo híbrido vs. lineal).
  - Confianza autorreportada: pasa de "reflexiono sobre cómo" a "ya sé cómo".
  - Leading indicator de Fase 2: % de padres que habilitan la billetera del hijo.
- **Promesa central:** *"No tienes que tener todo resuelto. Skandia te acompaña a enseñarle a tu hijo — un paso a la vez."*

---

## 2. Clasificación de riesgo

| Dimensión | Nivel | Razón |
|---|---|---|
| Regulatorio | 🟡 Medio | El método es guía/contenido — riesgo bajo. **Dos focos suben el nivel:** (a) el **motor generativo** hablando de plata con padres (no puede prometer rendimientos ni asesorar) y (b) las features de producto (Metas, Universidad) que heredan los pendientes de Fase 2. |
| Usabilidad | 🟡 Medio | Un solo actor, adulto, en un portal que ya usa. El reto se desplaza a **engagement y cadencia** — y a que el set de 4 features no se sienta como un **menú pasivo** sin el coach que lo sostiene. |
| Técnico | 🟡 Medio | Sin saldo en tiempo real ni PIN bidireccional en Fase 1. El reto técnico es el **motor generativo (LLM)**, el tablero del educador y la integración con el catálogo de productos. Gemini ya está cableado en el scaffold. |
| Negocio | 🟡 Medio-Alto | Adquisición de segmento nuevo + riesgo reputacional, pero experimento barato y reversible. Riesgo principal: que el método no enganche más que el curso. |

**Nivel compuesto: 🟡 AMARILLO — Riesgo Medio** (vs. ROJO 4/4 de la Fase 2).

**Implicación:** La Fase 1 puede avanzar a diseño y validación. Las definiciones bloqueantes de Legal/Ops/Producto se concentran en el **motor generativo** y en las **features de producto** (Metas, Universidad), y se afrontan con demanda ya validada.

---

## 3. Estructura del flujo

**Tipo:** Journey de un solo protagonista (el padre) con un **arranque secuencial corto** (diagnóstico → conciencia) y luego un **hub no lineal** (las 4 features) sostenido por un coach con cadencia.

```
 P01 entrada → P02 diag padre → P03 diag hijo → P04 TU RESULTADO (conciencia, LLM)
                                                            │
                                                            ▼
                                   P05 HOME / dashboard (coach híbrido + 4 features)
                                   ┌──────────────┬──────────────┬──────────────┐
                                   ▼              ▼              ▼              ▼
                              P06/P07 PLANES   P08 METAS    P10 UNIVERSIDAD  P11 CURSOS
                                            (P09 billetera = motor de Metas)
```

**El arranque (P01→P04) es lineal y obligatorio** — es lo único que el padre recorre en orden, porque sin diagnóstico no hay conciencia ni personalización. **De P05 en adelante es híbrido:** el coach recomienda y prioriza, pero el padre toma las features en el orden que quiera. Donde el orden importa, **fricción suave, no rejas.**

---

## 4. Arquitectura de información

> **11 pantallas.** El arranque (P01–P05) es el núcleo del experimento. Las features (P06–P11) cuelgan del home. P09 (billetera, cara del padre) reutiliza el MVP React existente.

---

### Pantalla 01 — Punto de entrada en el portal (entry-padre)

- **Job:** Que el padre descubra el método desde el portal Skandia que ya usa y entienda en una línea qué le ofrece.
- **Dos puntos de acceso:** (1) **tarjeta** destacada en el home del portal y (2) **ítem permanente en el menú lateral**. El prototipo muestra ambos.
- **Jerarquía:** 1) tarjeta + ítem de menú (label corto) · 2) promesa en una línea (perspectiva del padre) · 3) CTA de entrada.
- **Componentes sk-*:** `sk-card` · `sk-button` (primary).
- **Microcopy provisional:**
  - Título tarjeta: "Enséñale a tu hijo a manejar su plata."
  - Subtítulo: "Un método de Skandia para acompañarte, paso a paso. No necesitas saber de finanzas."
  - CTA: "Empezar"
- **Transición:** → P02.

---

### Pantalla 02 — Diagnóstico del padre (diag-padre)

- **Job:** Sacar la historia del padre con el dinero — la base de la conciencia. Es la mitad del espejo.
- **Jerarquía:** 1) encuadre que baja la guardia ("no hay respuestas malas") · 2) 4 preguntas cortas · 3) barra de avance breve · 4) CTA.
- **Las 4 preguntas (de "Crecer Juntos" Módulo 1):**
  1. ¿Cómo se hablaba de dinero en tu hogar de niño? (abiertamente / solo en dificultades / poco / casi nada)
  2. ¿Qué frase sobre el dinero escuchabas? ("hay que ahorrar" / "el dinero no alcanza" / "hay que trabajar muy duro" / no recuerdo)
  3. ¿Cómo es tu relación actual con el dinero? (organizada y tranquila / organizada pero estresante / me genera ansiedad / estoy aprendiendo)
  4. ¿Qué te gustaría que tu hijo aprendiera que tú no aprendiste? (abierta)
- **Componentes sk-*:** `sk-radio` · `sk-textarea` (P4 abierta) · `sk-progressbar` · `sk-card` · `sk-button` (primary).
- **Microcopy provisional:**
  - Título: "Antes de tu hijo, hablemos de ti."
  - Encuadre: "No hay respuestas buenas ni malas. Esto me ayuda a darte lo que sí te sirve."
  - CTA: "Siguiente: cuéntame de tu hijo"
- **Restricciones:** 🟡 Máx. 4 preguntas — el research advierte abandono por exceso de pasos. La P4 abierta alimenta el LLM; las cerradas alimentan las reglas-marco.
- **Transición:** → P03.

---

### Pantalla 03 — Diagnóstico del hijo, respondido por el padre (diag-hijo)

- **Job:** Capturar **cómo el padre ve a su hijo** con la plata — la otra mitad del espejo. **Es percepción, no la voz del hijo**, y se nombra honesto en pantalla.
- **Nota de honestidad obligatoria en pantalla:** "Esto es cómo **ves** a [nombre]. Más adelante, él/ella podrá contarnos su versión." (respeta el corte de alcance: no hay pantalla del hijo en Fase 1).
- **Jerarquía:** 1) datos (nombre + edad del hijo) · 2) 4 preguntas cortas · 3) barra de avance · 4) CTA.
- **Las 4 preguntas (de "Crecer Juntos" Módulo 2):**
  1. ¿Cómo describirías su relación con el dinero? (le gusta ahorrar / gasta rápido / curioso y pregunta / sin interés aún / no hemos hablado)
  2. Cuando recibe dinero, generalmente… (lo ahorra / gasta una parte y guarda / lo gasta rápido / depende)
  3. ¿Con qué frecuencia hablan de dinero? (frecuentemente / algunas veces / casi nunca) ← **variable que más pesa en el arranque**
  4. ¿Qué te gustaría enseñarle principalmente? (ahorro / tomar decisiones / prepararlo para la universidad / responsabilidad / independencia)
- **Componentes sk-*:** `sk-input` (nombre) · `sk-inputnumber` (edad) · `sk-radio` · `sk-progressbar` · `sk-button` (primary).
- **Microcopy provisional:**
  - Título: "Ahora, cuéntame de [nombre]."
  - CTA: "Ver lo que esto me dice"
- **Restricciones:** 🟡 La edad del hijo y la frecuencia de conversación son las dos variables que más mueven la recomendación del motor — validar que se capturen sin ambigüedad.
- **Transición:** → P04 (dispara la generación del resultado).

---

### Pantalla 04 — Tu resultado / La conciencia (resultado-conciencia) · GENERADA POR LLM

- **Job:** Pantalla bisagra y corazón del modelo. Devolver una **lectura personalizada del perfil familiar** que produzca el momento *"esto es para mí"* — y desde ahí presentar las 4 features ya activas. Es lo que dispara la acción.
- **Jerarquía:**
  1. **La lectura de conciencia** (texto generado por LLM): la frase que el padre heredó y puede estar transmitiendo · la brecha entre cómo es él y cómo ve al hijo · la **ventana de tiempo** (años antes de los 18 / universidad). Cálido, sin culpa.
  2. **Lo que sigue**: la acción recomendada de esta semana (también generada), como puente a la acción.
  3. **Tus herramientas**: las 4 features, ya desbloqueadas y **priorizadas** por el motor (no bloqueadas — híbrido).
  4. CTA hacia el home del método.
- **Componentes sk-*:** `sk-card` (bloque de conciencia, tratamiento visual destacado) · `sk-chip` ("Tu punto de partida") · `sk-card` ×4 (features, con orden/jerarquía visual según prioridad) · `sk-button` (primary) → "Ir a mi método".
- **Microcopy — ejemplo generado para Andrés/Valentina (ilustrativo, NO hardcodear):**
  > "Andrés, creciste oyendo 'el dinero no alcanza'. Eso te volvió cuidadoso, pero el silencio no protege a Valentina de esa sombra: se la transmite. Ella gasta rápido porque a los 16 aún no ha tenido que decidir nada importante con su plata — y te quedan unos 2 años antes de que se vaya a la universidad y la maneje sola. No tienes que volverte experto. Tienes que empezar a hablar."
  - Acción recomendada (ejemplo): "Esta semana, 10 minutos: pregúntale qué quiere estudiar y dónde. Aún no es una charla de plata — es abrir la puerta."
- **Restricciones:** 🔴 **El texto sale del LLM con guardrails (ver §5).** Nunca promete rendimientos, no da asesoría específica, no inventa datos del hijo más allá de lo ingresado. 🟡 Definir el tratamiento visual de un bloque de texto de longitud variable.
- **Transición:** → P05.

---

### Pantalla 05 — Home del método / Dashboard del educador (home-padre)

- **Job:** El hub al que el padre vuelve con la cadencia. Arriba, el **coach** con la acción de la semana (lo más prominente). Debajo, las **4 features** siempre visibles. Y su **progreso como educador**.
- **Jerarquía:**
  1. **El coach — la acción de esta semana** (generada, accionable, 5–10 min). Lo más prominente.
  2. Las **4 features** como accesos (tarjetas), priorizadas pero todas disponibles.
  3. **Progreso del padre como educador** (acciones hechas, conversaciones, features activadas).
  4. Acceso a la billetera si ya la activó (puente a Fase 2 del hijo).
- **El coach es híbrido:** recomienda y resalta una feature, pero ninguna está bloqueada. Donde el orden importa, **fricción suave** en la tarjeta de la feature: *"Puedes crear una meta ya. Pero como casi no hablan de plata, te rinde más empezar por la conversación."*
- **Componentes sk-*:** `sk-card` (acción de la semana, hero) · `sk-card` ×4 (features) · `sk-progressbar` + `sk-badge` (progreso del educador) · `sk-chip` (estado por feature) · `sk-button` (primary/secondary).
- **Microcopy provisional:**
  - Título: "Tu método, [nombre del padre]."
  - Acción semanal: "Esta semana: [acción generada]. Te toma [X] minutos."
  - Estado vacío: "Ya hiciste lo de esta semana. Te aviso cuando venga lo siguiente."
  - Progreso: "Has tenido [N] conversaciones con [nombre del hijo]. Vas activando tu método."
- **Restricciones:** 🟡 Definir qué cuenta como progreso del educador y de dónde sale el dato. 🟡 La acción de la semana se regenera con cadencia — definir disparador (ver decisiones pendientes).
- **Transición:** Hub central → P06/P07 (Planes), P08 (Metas), P10 (Universidad), P11 (Cursos), P09 (billetera).

---

### Pantalla 06 — Feature PLANES para crear conciencia (planes-lista)

- **Job:** El banco de experiencias del método — lo que crea la cadencia. Segmentado por **a quién sirve**, no por categoría técnica.
- **Tres segmentos (el eje del usuario):**
  - **Para ti** → el padre trabaja su propia relación con la plata (ej. "revisa la frase que heredaste").
  - **Para tu hijo** → experiencias que el hijo hace con acompañamiento (ej. "el reto de las 48 horas", "una semana sin compras impulsivas").
  - **En familia** → conversaciones y experiencias conjuntas (ej. "la caja de preguntas", "juntos al supermercado", "¿qué harías si…?").
- **Jerarquía:** 1) la experiencia recomendada por el coach, destacada · 2) los 3 segmentos con sus experiencias · 3) tag de categoría (conversación / consumo / autonomía) como filtro secundario.
- **Componentes sk-*:** `sk-card` (cada experiencia) · `sk-chip` (segmento + "Recomendada esta semana") · `sk-tag` (categoría) · `sk-accordion` (agrupar por segmento).
- **Microcopy provisional:**
  - Título: "Planes para crecer juntos."
  - Encuadre: "Pequeñas experiencias que vuelven natural hablar de plata en casa. Empieza por la que te recomiendo, o elige la tuya."
- **Restricciones:** 🟡 El catálogo de experiencias y su mapeo a segmentos/categorías es producción de contenido (base: "Crecer Juntos" Módulo 3, 9 experiencias). Kiki + experto pedagógico.
- **Transición:** → P07 (detalle de una experiencia).

---

### Pantalla 07 — Detalle de un plan + guion + registrar (plan-detalle)

- **Job:** Abrir una experiencia, dar el **guion de conversación** (lo que el padre no sabe hacer — el método se lo entrega masticado) y permitir **marcar que la hizo**. Es el dato que mide el éxito real.
- **Jerarquía:** 1) objetivo de la experiencia · 2) cómo hacerlo (pasos cortos) · 3) **la conversación: 2–3 abridores según el carácter del hijo** (el callado / el que ya pregunta / el desinteresado) — reúso de los guiones de Kiki · 4) qué hacer si se complica · 5) **registrar la acción** y cómo salió · 6) profundidad opcional (link al curso del Channel relevante).
- **Componentes sk-*:** `sk-card` (cada abridor) · `sk-chip` (tipo de hijo) · `sk-accordion` ("si se complica" / profundidad) · `sk-radio` (cómo salió: fluyó / costó / no se dio) · `sk-toast` (confirmación) · `sk-button` (primary) → "Ya lo hicimos".
- **Microcopy provisional:**
  - Abridor (hijo callado): "¿Alguna vez te has preguntado de dónde sale la plata que tenemos en casa?"
  - Si se cierra: "Si no quiere hablar, no insistas. El solo hecho de abrirlo ya cuenta."
  - Al registrar: "Lo hiciste. Eso es lo que cuenta." · "¿Cómo te fue?" → Fluyó / Me costó / No se dio · si "no se dio": "Tranquilo. Te la dejo para la próxima, sin presión."
- **Restricciones:** 🟡 Guiones = contenido sensible, revisión obligatoria de Kiki (tono no condescendiente, sin clichés de "papá perfecto"). 🟡 Confirmar con negocio que "acción completada" es la métrica norte.
- **Transición:** Al registrar → vuelve a P05 con el progreso actualizado; el coach propone el siguiente paso.

---

### Pantalla 08 — Feature METAS financieras (metas)

- **Job:** Que el padre cree una meta de ahorro con su hijo, **asociada a un producto Skandia**, y la siga. Es el funnel a producto. Se fondea con la billetera (P09).
- **Jerarquía:** 1) crear meta (nombre, monto objetivo, fecha) · 2) **asociar a un producto Skandia** (desde catálogo acotado) · 3) estado de la meta con progreso · 4) acción de fondear (→ P09).
- **Fricción suave (híbrido):** si la frecuencia de conversación es baja, la tarjeta sugiere conversar primero, sin bloquear.
- **Componentes sk-*:** `sk-input` · `sk-inputnumber` · `sk-select` (producto, catálogo) · `sk-progressbar` · `sk-card` · `sk-button` (primary).
- **Microcopy provisional:**
  - Título: "Una meta que persiguen juntos."
  - Ej. meta: "Mis Air Force 1 · $180.000" o "Fondo universidad de [nombre]".
  - Asociar producto: "Esta meta crece en: [producto Skandia]."
- **Restricciones:** 🔴 La asociación a producto y cualquier proyección heredan los pendientes de Legal/producto de Fase 2. **No prometer rendimientos.** 🟡 Definir el catálogo de productos elegibles para menores.
- **Transición:** → P09 (fondeo, cara del padre).

---

### Pantalla 09 — Billetera, cara del padre / motor de Metas (billetera-padre) — REÚSO DEL MVP

- **Job:** El padre **activa la billetera Kids desde su portal** y **fondea** la meta (aporte directo o aprobar una solicitud). Es la cara del padre de la billetera y el **motor de la feature Metas**. **Ya construido en `producto_skandia_kids` (React).**
- **Reúso:** el MVP existente — dashboard parental, aprobar solicitud de aporte con PIN, aporte directo, confirmación (toast). Alinear el dato de ejemplo a **Valentina, 16**.
- **Componentes sk-*:** los del MVP (`sk-card`, `sk-button`, `sk-inputmask` (PIN), `sk-toast`, `sk-dialog`).
- **🚧 Lo que NO se diseña aquí:** la **visual/interfaz del hijo** — cómo el adolescente ve y mueve su billetera. Eso es Fase 2.
- **Restricciones:** 🔴 Aviso legal de operaciones con productos de menores marcado como "⚠️ Pendiente Legal/Ops".
- **Transición:** Desde P08. Tras fondear, vuelve a Metas/Home con el progreso actualizado.

---

### Pantalla 10 — Feature PLANEACIÓN UNIVERSITARIA (universidad)

- **Job:** La gran meta — el detonante emocional del segmento. Ayudar al padre (y al hijo) a imaginar y costear la universidad, y conectar con una solución de ahorro/inversión.
- **Jerarquía:** 1) las preguntas-sueño (qué estudiar, dónde, qué experiencias) · 2) costo estimado y horizonte · 3) estrategia sugerida (ahorro periódico, becas, producto orientado a educación) · 4) CTA a crear la meta universitaria (→ P08).
- **Componentes sk-*:** `sk-card` · `sk-input`/`sk-select` · `sk-inputnumber` · `sk-accordion` (componentes del costo) · `sk-button` (primary).
- **Microcopy provisional:**
  - Título: "La universidad de [nombre] empieza hoy."
  - Encuadre: "No se trata de tener la plata lista, sino de empezar a planearla juntos."
- **Restricciones:** 🔴 La "estrategia financiera" y cualquier recomendación de producto de inversión orientado a educación **requieren validación de Legal** y salen de catálogo acotado — no texto libre del LLM. **No prometer rendimientos.**
- **Transición:** → P08 (crear meta universitaria) o P11 (curso relacionado).

---

### Pantalla 11 — Feature CURSOS para profundizar (cursos-channel)

- **Job:** La profundidad opcional. Los 2 cursos del Channel viven aquí, **partidos por tema** y enganchados a la feature donde importan — no como bloque de 2h impuesto.
- **Jerarquía:** 1) encuadre (opcional, para profundizar) · 2) módulos por tema · 3) "recomendado para lo que estás trabajando" · 4) acceso al curso completo.
- **Componentes sk-*:** `sk-card` · `sk-accordion` · `sk-tag` (tema) · `sk-chip` ("Recomendado") · `sk-button` (tertiary).
- **Microcopy provisional:**
  - Título: "Para cuando quieras profundizar."
  - Encuadre: "No tienes que ver nada de esto para avanzar. Está aquí si quieres saber más."
- **Restricciones:** 🟡 Requiere despiece de los 2 cursos del Channel por módulo/tema y mapeo a features. Con el equipo de contenido del Channel.
- **Regla de diseño:** el método empuja la **acción** (P07); el curso es la **profundidad** para quien la pide. Nunca al revés.
- **Transición:** Accesible desde P05 y desde las features relacionadas.

---

## 5. El motor generativo (LLM) — marco y guardrails

> Decisión 23 jun: el resultado de conciencia (P04) y la acción de la semana (P05) son **generados por LLM**, no plantillas fijas. Gemini ya está cableado en el scaffold (`metadata.json` → `SERVER_SIDE_GEMINI_API`). Modelo definitivo = decisión técnica posterior.

**Entrada (del diagnóstico P02+P03):** las 8 respuestas + nombre y edad del hijo.

**Variables-marco que el prompt debe razonar** (las reglas son guía del modelo, no código):
- `frecuencia_conversación` → punto de arranque (si "casi nunca" → empezar por conversación, no por Metas).
- `edad_hijo` → urgencia y ventana de tiempo ("te quedan ~X años").
- `comportamiento_hijo` → skill a priorizar (gasta rápido → autocontrol/decisiones).
- `perfil_padre` (frase heredada + relación actual) → tono + si activa un "plan para ti".
- `objetivo_declarado` → feature destacada en el dashboard.

**Salida estructurada esperada:**
1. `lectura_conciencia` — texto cálido y personalizado (la frase heredada, la brecha, la ventana).
2. `accion_semana` — una micro-acción concreta (5–10 min) con su porqué.
3. `orden_features` — prioridad sugerida de las 4 (no bloqueo).

**🔴 Guardrails (system prompt — innegociables, Legal):**
- **No** promete ni insinúa rendimientos, retornos o resultados financieros.
- **No** da asesoría financiera específica ni recomienda montos de inversión.
- Las recomendaciones de **producto Skandia salen de un catálogo acotado** que se le pasa al modelo — **no** las inventa en texto libre.
- **No** inventa datos del hijo más allá de lo ingresado.
- Tono: adulto, cálido, **sin culpa, sin "papá perfecto"**, español Colombia, longitud acotada.
- Salida pasa por **validación** antes de mostrarse (filtro de términos prohibidos / fallback a texto plantilla si falla).

---

## 6. Principios de diseño para este caso

1. **El padre es el protagonista — por ahora.** El hijo aparece como resultado de lo que el padre hace, no como segundo actor en pantalla.
2. **Acción sobre contenido.** Lo más prominente del home es la acción de la semana, no el material para leer. Si esto se siente como un curso, fracasa.
3. **El coach guía, no encierra (híbrido).** Recomienda y prioriza, pero el padre —adulto en su portal— nunca queda bloqueado. Fricción suave, no rejas.
4. **El método baja la presión, no la sube.** Normaliza la torpeza, permite "no se dio esta vez" sin castigo, celebra el paso pequeño.
5. **La conversación es el corazón.** Los guiones se sienten de una persona real, nunca de un manual.
6. **Soltar es el objetivo, no controlar.** El método se mide por la *graduación* del hijo a los 18.
7. **La personalización es generativa pero acotada.** El LLM redacta; Legal pone los límites. Nunca promete rendimientos ni reemplaza asesoría.
8. **La billetera se diseña por la cara del padre; la visual del hijo no** (Fase 2).

---

## 7. Decisiones pendientes antes de producción

- 🔴 **Guardrails del motor generativo:** validación de Legal del system prompt, catálogo de productos acotado, mecanismo de fallback. Bloqueante de P04/P05/P08/P10.
- 🟡 **Canal de cadencia:** cómo "el método te busca" (notificación del portal, correo, ambos) y qué dispara la regeneración de la acción de la semana.
- 🟡 **Producción de contenido — Planes:** catálogo de experiencias (base "Crecer Juntos" M3), mapeo a segmentos para-ti/hijo/familia. Kiki + experto pedagógico.
- 🟡 **Copy de los diagnósticos y plantillas de fallback** del resultado generativo. Kiki.
- 🟡 **Catálogo de productos Skandia** elegibles para menores (Metas, Universidad). Con producto.
- 🟡 **Despiece de los cursos del Channel** por tema y mapeo a features. Con el Channel.
- 🟡 **Tablero del educador:** qué cuenta como progreso y de dónde sale el dato. Afecta P05.
- 🔴 **Features de producto (Metas, Universidad):** heredan los pendientes legales/técnicos de Fase 2 (aviso legal, PIN, endpoint de saldo, producto de inversión para menores).
- 🟡 **Research — autonomía vs. control:** sprint pendiente; alimenta las experiencias "para tu hijo".
- 🟡 **Marca:** "Skandia Kids" describe al producto del hijo; el método podría necesitar nombre propio. "Crecer Juntos" en evaluación.

---

## 8. Instrucción a Rachel

- **Entregable:** Prototipo `.html` autocontenido — **desktop**, simulando el shell del portal Skandia con la sección del método dentro.
- **🚧 Alcance: la cara del padre.** La billetera solo del lado del padre (P09, reúso del MVP). **NO diseñar la visual del hijo.**
- **Punto de entrada:** P01 con sus **dos accesos** (tarjeta en el home del portal + ítem en el menú lateral).
- **Prioridad de prototipado:**
  1. **El arranque (el corazón del experimento):** P01 → P02 (diag padre) → P03 (diag hijo) → **P04 (conciencia)** → P05 (home/dashboard).
  2. La feature **Planes**: P06 → P07 (con guion + registrar). Es la cadencia.
  3. **Metas** (P08) + **billetera** (P09, reúso del MVP).
  4. **Universidad** (P10) y **Cursos** (P11) después.
- **P04 es la pantalla clave nueva** — diséñala para texto de longitud variable (sale del LLM). En el prototipo, usa el ejemplo de Andrés/Valentina como contenido vivo.
- **El coach manda en el home:** la acción de la semana es el elemento más prominente; las 4 features debajo, priorizadas pero todas accesibles (híbrido, sin bloqueos).
- **Tono visual:** Skandia adulto — serio, confiable, cálido. Nada infantil (eso es del hijo, Fase 2). Acompañamiento, no gamificación.
- **Microcopy provisional** — Kiki construye la voz antes de producción.
- **Elementos 🔴** (features de producto, billetera): aviso "⚠️ Pendiente Legal/Ops". Sin endpoint real.
- **Caso de ejemplo:** Andrés (50) / Valentina (16). (El MVP trae "Valentina Ríos 15" — alinear a 16.)

---

## 9. Señal de handoff a Kiki (Modo Content Designer)

Kiki recibe para construir/ajustar la voz del método con el nuevo espinazo:
- **Voz:** Adulto, cálido, sin culpa, sin jerga, sin "papá perfecto".
- **Producción prioritaria:**
  - Copy de los **dos diagnósticos** (P02, P03) y la **nota de honestidad** del diagnóstico del hijo.
  - **Plantillas de fallback** del resultado de conciencia (P04) — para cuando el LLM falle el guardrail.
  - El **catálogo de experiencias** de Planes (P06/P07), segmentado para-ti/hijo/familia, con sus guiones de conversación (los ya producidos se reubican aquí).
  - El microcopy de registro de acción (P07) que celebra sin condescender y permite "no se dio" sin castigo.
- **Puntos de atención:**
  - Que la acción siempre pese más que el contenido.
  - Que el tono baje la presión, no la suba.
  - Coherencia con los **guardrails de Legal** del motor generativo (§5).

---

*Skandia UX Team · #UXplorers · Junio 2026 · Rev. 23 jun (espinazo diagnóstico → conciencia → features).*
*Fase 1 del experimento Skandia Kids — re-centrado en el padre. La billetera del hijo es la Fase 2 (skandia-kids-PRD.md).*
