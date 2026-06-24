# PRD — Skandia Kids · El Método (Fase 1, centrado en el padre)
**Fecha:** 20 de junio de 2026
**Estratega:** Skandia UX Team · #UXplorers
**Para:** Rachel (ux-ui-designer)
**Insumos:** skandia-kids-northstar.md ✅ · skandia-kids-research.md ✅ (actualizado con datos del curso) · skandia-kids-PRD.md → se reubica como **Fase 2**
**Nota de contenido:** ⚠️ El microcopy del método para el padre es **voz nueva** no cubierta por skandia-kids-content.md. Todo el copy de este PRD es **provisional, pendiente de Kiki**.

---

## 1. Contexto

- **Caso:** Experimento de educación financiera familiar re-centrado en el **padre/cuidador** como protagonista. El producto deja de ser una billetera para el adolescente y pasa a ser un **método de crianza financiera** que vuelve capaz al padre de enseñar. El hijo y la billetera entran en la **Fase 2** (el PRD original).
- **Canal:** Vive **dentro del portal web Skandia existente** (sección dedicada), no es app ni producto independiente. El padre entra con sus credenciales actuales. La capa de cadencia ("el método te busca") se resuelve por notificaciones del portal y/o correo — ver decisión pendiente.
- **Segmento principal — padre/cuidador:** *Family Guardian*. Educación financiera empírica: nunca recibió el método de sus propios padres. Muy motivado (1.281 se inscribieron solos al curso del Channel) pero el formato pasivo lo pierde (~9,4% lo termina). Detonante emocional: la universidad.
- **Segmento secundario — adolescente (13–17):** su **interfaz** es Fase 2. La cara del padre de la billetera sí se diseña ahora.
- **🚧 Alcance de diseño Fase 1 — la cara del padre:** La billetera **sí entra en Fase 1, pero solo desde el lado del padre**: activarla desde el portal, fondearla y ver el progreso del hijo. Estas pantallas reutilizan las **pantallas parentales del PRD original** (su P01 activación, P07 aporte directo, P12 dashboard parental). Lo que **NO se diseña en Fase 1 es la visual/interfaz del hijo** — ninguna pantalla del adolescente (su dashboard, su vista de la billetera, crear metas, hacer crecer). Eso es Fase 2 (skandia-kids-PRD.md). **Nombre de trabajo:** "Skandia Kids" (provisional, decisión de marca pendiente).
- **Outcome de negocio:** Demostrar que Skandia puede ser el **aliado de confianza en la crianza financiera de la familia** — convirtiendo padres motivados que el formato curso perdió en padres que sí enseñan, y abriendo la puerta natural a la billetera del hijo (Fase 2) y a producto.
- **Problema del usuario (padre):** *"Quiere enseñarle a su hijo a manejar el dinero pero no tiene la herramienta ni el método."* La herramienta existe; el método no — y no lo tiene porque a él nunca se lo dieron.
- **Cómo medir el éxito:**
  - El padre completa **al menos una acción/conversación real** con su hijo (no "contenido visto"). Meta: batir por amplio margen el baseline del **9,4%** de finalización del curso.
  - Cadencia sostenida: el padre vuelve, no abre-una-vez.
  - Confianza autorreportada: pasa de "reflexiono sobre cómo" a "ya sé cómo".
  - Leading indicator de Fase 2: % de padres que habilitan la billetera del hijo.
- **Promesa central:** *"No tienes que tener todo resuelto. Skandia te acompaña a enseñarle a tu hijo — un paso a la vez."*

---

## 2. Clasificación de riesgo

| Dimensión | Nivel | Razón |
|---|---|---|
| Regulatorio | 🟡 Medio | El método en sí es guía/contenido — riesgo bajo. La **activación de la billetera** (Etapa 2) hereda los pendientes legales de la Fase 2, pero ya no abre la Fase 1 a riesgo transaccional. |
| Usabilidad | 🟡 Medio | Un solo actor, adulto, en un portal que ya usa. Desaparece la bifurcación de actor y el doble modelo mental. El reto se desplaza a **engagement y cadencia** (vencer el abandono del curso), no a la fricción transaccional. |
| Técnico | 🟡 Medio | Sin saldo en tiempo real ni PIN bidireccional en Fase 1. El reto técnico es el **motor de cadencia/personalización** y el **tablero de progreso del educador**. La activación de billetera (Etapa 2) hereda la integración de la Fase 2. |
| Negocio | 🟡 Medio-Alto | Sigue siendo adquisición de segmento nuevo y hay riesgo reputacional, pero el experimento es **más barato y reversible**. Riesgo principal: que el método no enganche más que el curso. |

**Nivel compuesto: 🟡 AMARILLO — Riesgo Medio** (vs. ROJO 4/4 de la Fase 2). El experimento se vuelve viable de validar antes de construir la maquinaria pesada.

**Implicación:** La Fase 1 puede avanzar a diseño y validación sin las definiciones bloqueantes de Legal/Ops/Producto, que se concentran en las etapas tardías (2 en adelante) y se afrontan cuando la demanda ya esté validada.

---

## 3. Estructura del flujo

**Tipo:** Journey longitudinal de un solo protagonista (el padre), no un flujo de una sesión.

El método no se "completa" de una; se **recorre en el tiempo**, etapa por etapa, con cadencia semanal. El arco emocional del padre va de *"no sé cómo enseñarle"* → *"ya sé cómo, y mi hijo se está graduando"*. Hay un solo carril; el hijo aparece como consecuencia de las acciones del padre, no como segundo actor de la interfaz.

### El arco (7 etapas)

| # | Etapa | El padre logra que su hijo… | Billetera — cara del padre (Fase 1) / visual del hijo (Fase 2) |
|---|---|---|---|
| 0 | Tu punto de partida | — (diagnóstico y autoconciencia del padre) | — |
| 1 | La primera conversación | …hable de dinero sin que sea sermón | — |
| 2 | Plata propia | …vea y controle un monto suyo | 🔓 **F1:** el padre activa y fondea la billetera (P09) · **F2:** la visual del hijo |
| 3 | Decidir y equivocarse | …decida gastos y se equivoque barato | F2: uso libre del saldo (visual del hijo) |
| 4 | Metas | …quiera algo y planee para lograrlo | F2: metas + aportes/retiros con PIN (visual del hijo) |
| 5 | Hacer crecer | …entienda guardar vs. invertir | 🔴 Momento 6 (bloqueado Legal/producto) |
| 6 | Rumbo a los 18 | …se gradúe: maneje su plata solo | handoff a producto adulto |

**Punto de bisagra con la Fase 2:** la Etapa 2 ("Plata propia") es donde el método desemboca en la billetera. **En Fase 1 se diseña la cara del padre** (activar/fondear/seguir — P09, reúso de la activación parental del PRD original). **La visual del hijo sobre esa billetera, y todo el uso del adolescente (Etapas 3–4), es Fase 2.**

---

## 4. Arquitectura de información

> El método tiene **9 pantallas núcleo** (P01–P09). La de "Detalle de etapa" (P05) es una **plantilla que se repite** para las 7 etapas, no 7 pantallas distintas. P09 (activación de la billetera, cara del padre) reutiliza pantallas parentales del PRD original.

---

### Pantalla 01 — Punto de entrada en el portal (entry-padre)

- **Job:** Que el padre descubra el método desde el portal Skandia que ya usa y entienda en una línea qué le ofrece.
- **Dos puntos de acceso:** (1) **tarjeta** destacada en el home del portal y (2) **ítem permanente en el menú lateral** del portal. El prototipo debe mostrar ambos.
- **Jerarquía de contenido:**
  1. Tarjeta de acceso en el home del portal + ítem en el menú lateral (label corto)
  2. Promesa en una línea — desde la perspectiva del padre
  3. CTA de entrada al método
- **Componentes sk-*:** `sk-card` → tarjeta de acceso · `sk-button` (primary) → "Empezar"
- **Microcopy provisional:**
  - Título tarjeta: "Enséñale a tu hijo a manejar su plata."
  - Subtítulo: "Un método de Skandia para acompañarte, paso a paso. No necesitas saber de finanzas."
  - CTA: "Empezar"
- **Transición:** Va a P02 (diagnóstico).

---

### Pantalla 02 — Diagnóstico / Etapa 0 (diag-padre)

- **Job:** Ubicar el punto de partida — edad y madurez del hijo, qué ya hace con la plata, y la propia relación del padre con el dinero.
- **Jerarquía de contenido:**
  1. Encuadre que baja la guardia ("no hay respuestas malas")
  2. 3–4 preguntas cortas (edad del hijo · de dónde saca plata hoy · si hablan de dinero · qué te angustia de su futuro)
  3. Barra de avance breve (que se sienta de 3 min, no de cuestionario)
  4. CTA de cierre
- **Componentes sk-*:** `sk-radio` / `sk-checkbox` → respuestas · `sk-progressbar` → avance del diagnóstico · `sk-card` → contenedor por pregunta · `sk-button` (primary) → "Ver mi punto de partida"
- **Microcopy provisional:**
  - Título: "Antes de empezar, cuéntame de tu familia."
  - Encuadre: "No hay respuestas buenas ni malas. Esto solo me ayuda a darte lo que sí te sirve."
  - Ej. pregunta: "¿De dónde saca plata tu hijo hoy?" → mesada / regalos / su propio emprendimiento / no maneja plata todavía
  - CTA: "Ver mi punto de partida"
- **Restricciones:** 🟡 Validar con UX que el diagnóstico no supere 4 preguntas — el research advierte abandono por exceso de pasos.
- **Transición:** Va a P03 (resultado).

---

### Pantalla 03 — Tu punto de partida (resultado-diag)

- **Job:** Devolver el punto de entrada al método de forma personalizada y explicar por qué la siguiente etapa es la que es. Primer momento de "esto es para mí".
- **Jerarquía de contenido:**
  1. Lectura corta y cálida del diagnóstico (sin juicio)
  2. Tu etapa de entrada (puede no ser la 1 — un hijo de 17 arranca más adelante)
  3. Por qué empezamos ahí
  4. Vista previa del recorrido completo (las 7 etapas) para dar sentido de mapa
  5. CTA hacia el home del método
- **Componentes sk-*:** `sk-card` → tarjeta de resultado · `sk-steps` → vista del recorrido de 7 etapas · `sk-chip` → etiqueta "Tu etapa de entrada" · `sk-button` (primary) → "Ir a mi método"
- **Microcopy provisional:**
  - Título: "Tu hijo está listo para [tema de la etapa de entrada]."
  - Cuerpo: "Por lo que me contaste, no tiene sentido empezar de cero. Arrancamos en [Etapa X], donde [beneficio concreto]."
  - CTA: "Ir a mi método"
- **Restricciones:** 🟡 La lógica de asignación de etapa de entrada según diagnóstico debe definirse con UX/contenido (reglas por edad + madurez).
- **Transición:** Va a P04 (home del método).

---

### Pantalla 04 — Home del método / Tablero del educador (home-padre)

- **Job:** Pantalla central. El padre ve dónde va en el recorrido, cuál es **su micro-acción de esta semana**, su progreso como educador, y acceso a recursos. Es el hub al que vuelve con la cadencia.
- **Jerarquía de contenido:**
  1. **La micro-acción de la semana** — lo más prominente, lo accionable (no contenido)
  2. El recorrido de 7 etapas con la etapa actual marcada
  3. Progreso del padre como educador (etapas trabajadas, conversaciones hechas)
  4. Acceso a la etapa actual (detalle)
  5. Acceso al centro de recursos (cursos del Channel)
  6. Si ya desbloqueó la billetera: acceso al espacio del hijo (puente a Fase 2)
- **Componentes sk-*:** `sk-card` → tarjeta de la micro-acción de la semana · `sk-steps` → recorrido de etapas · `sk-progressbar` → progreso del educador · `sk-badge` → hitos del padre · `sk-button` (primary) → "Ver la acción de esta semana" · `sk-button` (secondary) → "Mi etapa actual" · `sk-chip` → estado por etapa (hecha / en curso / por venir)
- **Microcopy provisional:**
  - Título: "Tu método, [nombre del padre]."
  - Tarjeta acción semanal: "Esta semana: [micro-acción]. Te toma 5 minutos."
  - Progreso: "Vas [X] de 7 etapas. Has tenido [N] conversaciones con [nombre del hijo]."
  - Estado vacío de acción: "Ya hiciste lo de esta semana. Te aviso cuando venga lo siguiente."
- **Restricciones:** 🟡 Definir la fuente y el detalle del "tablero del educador" — qué cuenta como progreso (etapas, acciones, conversaciones marcadas).
- **Transición:** Hub central. Va a P05 (detalle de etapa), P07 (registrar acción), P08 (recursos) y — si aplica — al espacio del hijo (Fase 2).

---

### Pantalla 05 — Detalle de etapa (etapa-detalle) · PLANTILLA ×7

- **Job:** Abrir una etapa y entregar su anatomía completa. **Esta misma plantilla se instancia para las 7 etapas** — cambia el contenido, no la estructura.
- **Jerarquía de contenido (la anatomía fija del método):**
  1. Nombre y objetivo de la etapa
  2. **Concepto que vas a enseñar** (en lenguaje del padre, sin jerga)
  3. **Señales de que tu hijo está listo** (lista corta de chequeo)
  4. **La conversación clave** — el guion/abridor (corazón emocional) → enlaza a P06
  5. **La micro-acción de la semana** — qué hacer y CTA para marcarla → enlaza a P07
  6. Profundidad opcional: módulo del curso del Channel relevante a esta etapa
  7. Cuando aplica (Etapa 2): el desbloqueo de la billetera → P-bisagra
- **Componentes sk-*:** `sk-card` → bloques de la anatomía · `sk-accordion` → "señales" y profundidad opcional (no interrumpen el flujo) · `sk-chip` → "Coach Skandia" en el guion · `sk-button` (primary) → "Ver la conversación" / "Marcar mi acción" · `sk-tag` → etiqueta de la etapa · `sk-tooltip` → aclaración de conceptos nuevos
- **Microcopy provisional (ejemplo Etapa 1 — La primera conversación):**
  - Objetivo: "Que hablar de plata con tu hijo deje de ser un tema raro."
  - Concepto: "El dinero se puede hablar. Lo más difícil es la primera vez."
  - Señales: "Tu hijo… ya recibe algo de plata · te ha preguntado por precios · o evita el tema."
  - CTA a guion: "Ver cómo empezar la conversación"
  - Micro-acción: "Esta semana, ten una charla de 5 minutos. No tiene que ser perfecta."
- **Restricciones:** 🟡 El contenido de las 7 instancias es **producción de contenido nueva** — depende de Kiki + experto pedagógico. La Etapa 5 ("Hacer crecer") está 🔴 bloqueada por Legal hasta definir producto subyacente.
- **Transición:** Viene de P04. Va a P06 (guion), P07 (registrar acción), P08 (recurso) o al desbloqueo de billetera en la Etapa 2.

---

### Pantalla 06 — La conversación / guion (conversa-guion)

- **Job:** Dar al padre los abridores concretos para la conversación de la etapa y qué hacer si se complica. Es lo que el padre no sabe hacer — el método se lo entrega masticado.
- **Jerarquía de contenido:**
  1. 2–3 abridores según el carácter del hijo (el callado / el que ya pregunta / el desinteresado)
  2. Qué hacer si se cierra o sale mal
  3. Recordatorio de que la primera vez puede ser torpe (baja la presión)
  4. CTA para marcar que la tuvo
- **Componentes sk-*:** `sk-card` → cada abridor · `sk-chip` → tipo de hijo · `sk-accordion` → "si se complica" · `sk-button` (primary) → "Ya tuve la conversación"
- **Microcopy provisional:**
  - Abridor (hijo callado): "¿Alguna vez te has preguntado de dónde sale la plata que tenemos en casa?"
  - Si se cierra: "Si no quiere hablar, no insistas. Déjalo caer y vuelve otro día. El solo hecho de abrirlo ya cuenta."
  - Cierre: "No tiene que salir perfecta. Lo importante es que pasó."
  - CTA: "Ya tuve la conversación"
- **Restricciones:** 🟡 Los guiones son contenido sensible — revisión obligatoria de Kiki para tono no condescendiente y sin clichés de "papá perfecto".
- **Transición:** Viene de P05. Al marcar, va a P07.

---

### Pantalla 07 — Registrar la micro-acción (registro-accion)

- **Job:** Que el padre marque que hizo la acción/conversación y cómo le fue. Es el dato que mide el éxito real (acción, no contenido visto) y alimenta la personalización de la cadencia.
- **Jerarquía de contenido:**
  1. Confirmación cálida del logro
  2. Captura ligera de cómo salió (fluyó / costó / no se dio)
  3. Qué desbloquea o qué sigue
  4. CTA de continuar
- **Componentes sk-*:** `sk-toast` → confirmación · `sk-card` → captura de cómo salió · `sk-radio` → fluyó/costó/no se dio · `sk-button` (primary) → "Continuar" · `sk-badge` → hito sumado al tablero del educador
- **Microcopy provisional:**
  - Título: "Lo hiciste. Eso es lo que cuenta."
  - Pregunta: "¿Cómo te fue?" → Fluyó / Me costó un poco / No se dio esta vez
  - Si "no se dio": "Tranquilo. Te la dejo para la próxima semana, sin presión."
  - Cierre: "Sumaste un paso como educador de [nombre del hijo]."
- **Restricciones:** 🟡 Confirmar con negocio que "acción completada" (no contenido visto) es la métrica norte oficial del experimento.
- **Transición:** Viene de P05/P06. Vuelve a P04 (home) con el progreso actualizado.

---

### Pantalla 08 — Centro de recursos / Cursos del Channel (recursos-padre)

- **Job:** Albergar la profundidad opcional. Los cursos del Channel viven aquí, **partidos por tema** y enganchados a la etapa donde importan — no como bloque de 2h impuesto.
- **Jerarquía de contenido:**
  1. Encuadre: esto es opcional, para cuando quieras profundizar
  2. Módulos organizados por etapa del método
  3. Indicador de qué módulo conecta con tu etapa actual
  4. Acceso al curso completo del Channel para quien lo quiera
- **Componentes sk-*:** `sk-card` → cada módulo/recurso · `sk-accordion` → agrupación por etapa · `sk-tag` → etapa asociada · `sk-chip` → "Recomendado para tu etapa" · `sk-button` (tertiary) → "Ver módulo"
- **Microcopy provisional:**
  - Título: "Para cuando quieras profundizar."
  - Encuadre: "No tienes que ver nada de esto para avanzar. Está aquí si quieres saber más."
  - Etiqueta contextual: "Esto te sirve para tu etapa actual: [tema]."
- **Restricciones:** 🟡 Requiere despiece de los 2 cursos del Channel por tema/módulo y mapeo a etapas — trabajo conjunto con el equipo de contenido del Channel.
- **Regla de diseño:** El método empuja la **acción** (P07); el curso es la **profundidad** para quien la pide. Nunca al revés.
- **Transición:** Accesible desde P04 y desde P05 (profundidad de cada etapa).

---

### Pantalla 09 — Activación de la billetera, cara del padre (Etapa 2) — SÍ se diseña

- **Job:** En la Etapa 2 ("Plata propia"), el padre **activa la billetera Kids desde su portal** y define/fondea el monto que será del hijo. Es la cara del padre de la billetera — **sí entra en el diseño de Fase 1.**
- **Reúso:** Reutiliza la **activación parental del PRD original (su Pantalla 01)** y, para fondeo y seguimiento, las pantallas parentales P07 (aporte directo) y P12 (dashboard parental) de ese PRD.
- **Componentes sk-*:** `sk-card`, `sk-button` (primary), `sk-tooltip`, `sk-badge` (los de la activación parental original).
- **🚧 Lo que NO se diseña aquí:** la **visual/interfaz del hijo** — cómo el adolescente ve y mueve su billetera. Eso es Fase 2.
- **Microcopy:** ver banner de activación (vista del padre) en el bloque de Etapa 2 del content.md.
- **Transición:** Desde P05 (Etapa 2). El padre activa y fondea; el método continúa. La experiencia del hijo sobre esa billetera llega en Fase 2.

---

## 5. Principios de diseño para este caso

**1. El padre es el protagonista — por ahora.** Toda la interfaz refuerza que el método lo vuelve capaz a él. El hijo no es un segundo actor en pantalla; aparece como resultado de lo que el padre hace.

**2. Acción sobre contenido.** Lo más prominente de cada pantalla es la micro-acción de la semana, no el material para leer/ver. El baseline del 9,4% del curso es el recordatorio permanente: si esto se siente como un curso, fracasa.

**3. El método baja la presión, no la sube.** El padre llega con culpa e inseguridad ("a mí nadie me enseñó"). Cada pantalla normaliza la torpeza, permite "no se dio esta vez" sin castigo, y celebra el paso por pequeño que sea.

**4. La conversación es el corazón.** Lo más difícil para el padre es hablar de plata (tabú cultural documentado). Los guiones deben sentirse de una persona real, nunca de un manual ni de un "papá perfecto".

**5. Soltar es el objetivo, no controlar.** El recorrido se mide por la *graduación* del hijo a los 18. La estética y el lenguaje apuntan a autonomía creciente, no a vigilancia.

**6. La billetera se diseña por la cara del padre; la visual del hijo no.** En Fase 1 se diseña cómo el padre activa, fondea y sigue la billetera (P09). La interfaz del adolescente sobre esa billetera es Fase 2. Los cursos del Channel sí se integran (profundidad redesplegada), porque son contenido para el padre.

---

## 6. Decisiones pendientes antes de producción

- 🟡 **Canal de cadencia:** definir cómo "el método te busca" (notificación del portal, correo, ambos). Define si el experimento puede sostener la cadencia semanal que lo diferencia del curso.
- 🟡 **Lógica de asignación de etapa de entrada:** reglas por edad + madurez del hijo a partir del diagnóstico (P02→P03). UX + contenido.
- 🟡 **Definición de la métrica norte:** confirmar con negocio que "acción/conversación completada" (no contenido visto) es el éxito oficial. Afecta P07.
- 🟡 **Producción de contenido del método:** las 7 instancias de la plantilla de etapa (concepto, señales, guiones, micro-acciones) son contenido nuevo. Requiere Kiki + experto pedagógico.
- 🟡 **Despiece de los cursos del Channel:** partir los 2 cursos por módulo/tema y mapearlos a etapas. Con el equipo del Channel. Afecta P08.
- 🟡 **Tablero del educador:** definir qué cuenta como progreso del padre y de dónde sale el dato. Afecta P04.
- 🔴 **Etapa 5 "Hacer crecer":** bloqueada por Legal y por definición de producto subyacente — hereda el pendiente del Momento 6 del PRD Fase 2.
- 🔴 **Bisagra a Fase 2 (activación billetera):** hereda los pendientes legales/técnicos del PRD original (aviso legal, mecanismo de PIN, endpoint de saldo) — pero solo se afrontan al llegar a la Etapa 2, ya con demanda validada.
- 🟡 **Research — autonomía vs. control:** el sprint pendiente del research ahora tiene casa clara (Etapa 3). Recomendado validarlo antes de diseñar el detalle de esa etapa.
- 🟡 **Marca — nombre del método:** "Skandia Kids" describe al producto del hijo. El método para el padre podría necesitar nombre propio. Definición de marca.

---

## 7. Instrucción a Rachel

- **Entregable esperado:** Prototipo `.html` autocontenido — **desktop**, porque el padre vive en el portal web Skandia. El prototipo debe simular el shell del portal actual con la sección del método dentro, no como producto independiente.
- **🚧 Alcance: la cara del padre.** La billetera **sí se diseña, pero solo del lado del padre** (activar, fondear, ver progreso — P09, que reutiliza las pantallas parentales del PRD original). **NO diseñar la visual del hijo** — ninguna pantalla del adolescente (su dashboard, su vista de la billetera, crear metas, hacer crecer). Eso es Fase 2.
- **Punto de entrada:** Incluir P01 con sus **dos accesos** — tarjeta en el home del portal **y** ítem en el menú lateral.
- **Prioridad de prototipado:** 1) El núcleo del recorrido: P02 → P03 → P04 (home) → P05 (detalle de etapa) → P06 (guion) → P07 (registro). Ese loop es el experimento. 2) P08 (recursos) y P09 (activación de la billetera, cara del padre) después. **Ninguna pantalla del adolescente se prototipa.**
- **La plantilla de etapa (P05) es una sola pantalla parametrizable** — prototipar con la Etapa 1 como ejemplo vivo, y mostrar el recorrido completo en el `sk-steps` del home.
- **Tono visual:** El padre debe sentir que está en **Skandia adulto** — serio, confiable, cálido. Nada infantil aquí (eso es del hijo, en Fase 2). La energía es de acompañamiento, no de gamificación.
- **Lo accionable manda:** la micro-acción de la semana debe ser el elemento más prominente del home. El contenido/recursos siempre en segundo plano.
- **Microcopy:** todo el copy de este PRD es **provisional**. No tomarlo como final — Kiki construye la voz del método antes de producción.
- **Elementos 🔴** (Etapa 5, billetera/Fase 2): solo como texto "pendiente Legal / Próximamente (Fase 2)". Sin pantalla funcional detrás.

---

## 8. Señal de handoff a Kiki (Modo Content Designer)

Este PRD requiere **contenido nuevo** antes de poder pulir el prototipo. Kiki recibe para construir la voz del método para el padre:
- **Canal:** Portal web Skandia (padre/cuidador, *Family Guardian*).
- **Voz:** Adulto, cálido, sin culpa, sin jerga financiera, sin "papá perfecto". Acompaña, no enseña desde arriba.
- **Fuentes de verdad:** skandia-kids-northstar.md · skandia-kids-research.md · skandia-comunicacion · master-de-segmentacion.
- **Producción prioritaria:**
  - Las 7 instancias de la plantilla de etapa (concepto · señales · micro-acción).
  - Los **guiones de conversación** (P06) — lo más sensible y diferenciador.
  - El microcopy del registro de acción (P07) que celebra sin condescender y permite "no se dio" sin castigo.
- **Puntos de atención:**
  - Que la acción siempre pese más que el contenido.
  - Que el tono baje la presión del padre, no la suba.
  - Que el nombre del método (pendiente de marca) no se confunda con "Skandia Kids" (que es del hijo).

---

*Skandia UX Team · #UXplorers · Junio 2026*
*Fase 1 del experimento Skandia Kids — re-centrado en el padre. La billetera del hijo es la Fase 2 (skandia-kids-PRD.md).*
