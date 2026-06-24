# North-Star — Skandia Kids (re-centrado en el padre)
**Fecha:** 20 de junio de 2026 · **Rev. 23 de junio de 2026** (nuevo espinazo: diagnóstico → conciencia → features)
**Equipo:** Skandia UX Team · #UXplorers
**Propósito:** Ancla estratégica para reescribir research, contenido y PRD. Fija el reframe del experimento antes de tocar cualquier entregable derivado.
**Estado:** Insumos vigentes — skandia-kids-research.md (actualizado) · skandia-kids-content.md · skandia-kids-PRD.md (se reubica como Fase 2)

> **Rev. 23 jun:** el método deja de ser una **ruta lineal de 7 etapas** y pasa a un modelo **diagnóstico → conciencia → set de features que el padre activa**. Las secuencias obligatorias se fugan igual que el curso; este modelo es más activable, más medible por pieza y mete dos cosas nuevas: **diagnóstico del hijo** y un **gancho a producto Skandia explícito**. La motivación y el caso de ejemplo (Andrés, 50 / Valentina, 16) están en la sesión de diseño del 23 jun.

---

## El cambio de marco

> **Antes:** una billetera supervisada para que el adolescente desarrolle agencia financiera.
> **Ahora:** un **método de crianza financiera** que vuelve capaz al padre de enseñar — la billetera se vuelve lo que el padre desbloquea, no el punto de partida.

El protagonista del experimento, en esta fase, es **el padre**. El hijo entra después.

---

## El problema

El PRD original ya lo había escrito sin verlo del todo:

> *"Quiere enseñarle a su hijo a manejar el dinero pero no tiene la herramienta ni el método."*

La herramienta, en buena medida, ya existe (3 de cada 5 familias ya tienen un producto financiero para su hijo). **Lo que falta es el método** — y falta por una razón de raíz: a los padres **nunca se lo dieron**. Su educación financiera es empírica; no la recibieron de sus propios padres. No pueden transmitir un método que no tienen.

El job desatendido, entonces, no es (todavía) del hijo:

> *"Ayúdame a convertirme en un papá capaz de enseñarle a mi hijo sobre plata — dame el método, los momentos y las palabras — porque a mí nadie me enseñó."*

---

## La evidencia que lo respalda

El curso **"Educación financiera para padres"** del Skandia Channel es la prueba dura:

| Métrica | Valor | Lectura |
|---|---|---|
| Inscritos | 1.281 | La demanda es real y masiva — los padres levantan la mano solos |
| Certificados | 120 (~9,4%) | Pero el formato curso pierde a 9 de cada 10 |
| Estudio promedio | ~11 min/inscrito | El contenido pasivo no convierte intención en acción |

**Conclusión:** el cuello de botella no es interés, ni contenido, ni marca. Es el **formato**. Los padres no necesitan más para *ver*; necesitan algo que los haga *hacer*. Y un método **lineal y obligatorio** (la ruta de 7 etapas) reincide en parte del problema: las secuencias se fugan. Por eso el espinazo cambia a un modelo que diagnostica, genera conciencia y **abre opciones** en vez de imponer un orden.

---

## La promesa

**Skandia es el coach del padre.** No un curso que se ve una vez, sino un método con cadencia, personalizado y accionable.

| Curso (lo que ya falló) | Método (lo que proponemos) |
|---|---|
| "Ve y aprende" | "Haz esto con tu hijo esta semana" |
| Genérico | Personalizado al perfil de la familia (padre + hijo) |
| Se abre una vez | Tiene cadencia y te busca |
| Mide contenido visto | Mide conversaciones y acciones hechas |
| El protagonista es el contenido | El protagonista es el padre como educador |

**Lo que falló del curso fue el formato, no el contenido.** El material pedagógico es un activo: el método lo conserva y lo **redespliega** como una de las features (cursos del Channel, partidos por tema). El método es el empaque; los cursos son una de las cosas que entrega.

---

## La espina del método (rev. 23 jun) — tres movimientos, no siete etapas

```
 DIAGNÓSTICO            TU RESULTADO              EL MÉTODO EN MARCHA
 (padre → hijo)    →    (la conciencia)     →     (coach híbrido + 4 features)
```

**1 · Diagnóstico (padre, luego hijo).** Dos espejos cortos. El del padre saca su historia con el dinero (la frase heredada, su relación actual). El del hijo **lo responde el padre** — es su *percepción*, no la voz del hijo; se nombra honesto en pantalla ("así *ves* a tu hijo") y en Fase 2 el hijo responde directo. Esa brecha percepción-vs-realidad es oro para el futuro.

**2 · Tu resultado — la conciencia.** Un **LLM** devuelve una lectura personalizada del perfil familiar: la frase que el padre heredó y puede estar transmitiendo, la brecha entre cómo es él y cómo es el hijo con la plata, y la **ventana de tiempo** (los años que quedan antes de los 18 / la universidad). Es el momento *"esto es para mí"* que dispara la acción — no un reporte genérico.

**3 · El método en marcha — coach híbrido sobre 4 features.** El coach recomienda **una acción por semana** y prioriza el orden, pero **no bloquea**: las 4 features están a la vista y el padre toma lo que quiera, cuando quiera. Donde el orden importa, el coach pone **fricción suave**, no una reja (*"puedes crear una meta ya, pero como casi no hablan de plata, te rinde más empezar por la conversación — tú decides"*).

| Feature | Qué es | Gancho |
|---|---|---|
| **Planes para crear conciencia** | Banco de experiencias segmentado **para ti · para tu hijo · en familia**. El coach recomienda 1/semana según el diagnóstico. | Es la cadencia — lo que nos separa del curso. |
| **Metas financieras** | Metas asociadas a un **producto Skandia**; se fondean con la **billetera (cara del padre)** — el MVP React que ya existe. | El funnel a producto. |
| **Planeación universitaria** | La gran meta: carrera, ciudad, costo, horizonte. | El **detonante emocional** del segmento. |
| **Cursos para profundizar** | Los 2 cursos del Channel, **partidos por tema** y enganchados a la feature donde importan. | Segunda vida medible a un activo que hoy pierde al 91%. |

**El motor de personalización es generativo.** El resultado de conciencia y la acción de la semana los redacta un LLM (Gemini ya está cableado en el scaffold) guiado por reglas-marco: *frecuencia de conversación → punto de arranque · edad del hijo → urgencia · comportamiento → skill a priorizar · perfil del padre → tono y "plan para ti" · objetivo declarado → feature destacada.*

> 🔴 **Guardrail de Legal (por la decisión de motor generativo):** el LLM **no promete rendimientos ni da asesoría financiera específica**; la recomendación de soluciones Skandia sale de un **catálogo acotado**, no de texto libre del modelo. El tono (sin culpa, sin "papá perfecto") va en el system prompt. Se especifica en el PRD.

El padre tiene **su propio tablero de progreso** como educador — no solo el saldo del hijo. Esa es la inversión de protagonista.

---

## El hijo y la billetera

El PRD actual **no se desperdicia: se reubica como Fase 2.** En el nuevo espinazo, la billetera deja de ser una "etapa" y se vuelve **el motor de la feature Metas**: cuando una meta se asocia a un producto Skandia, el padre la fondea con el flujo de aprobar-con-PIN que ya existe (el MVP `producto_skandia_kids`).

**Corte de alcance Fase 1 (precisión clave):** la billetera **sí se diseña, pero solo por la cara del padre** — activarla, fondearla y ver el progreso (reúso de las pantallas parentales del PRD original). **La visual/interfaz del hijo** —cómo el adolescente ve y mueve su billetera, crea metas, hace crecer— **es Fase 2 y no se diseña ahora.** **El % de padres que llega a habilitar la billetera es el leading indicator de la Fase 2.**

---

## Outcome de negocio

> Demostrar que **Skandia puede ser el aliado de confianza en la crianza financiera de la familia** — convirtiendo a 1.281 padres motivados (que el formato curso perdió) en padres que sí enseñan, y abriendo la puerta natural a la billetera del hijo y, más adelante, a producto.

Es una cuña más pegajosa, recurrente y defendible que la original, y se apoya en el activo de marca que el research destaca: *Skandia = confianza para los padres.*

---

## Métricas (contra un baseline real)

- **Baseline a vencer:** el curso logra ~9,4% de finalización con horas de estudio pasivo.
- **Métrica norte:** % de padres que completan **al menos una acción/conversación real con su hijo** — porque el método pide minutos accionables, no horas de video. La meta es batir el 9% por amplio margen.
- **Engagement del padre:** acciones hechas, cadencia sostenida (no abre-una-vez), conversaciones marcadas como hechas.
- **Activación de features:** cuántas de las 4 toca el padre y en qué orden (valida el modelo híbrido vs. lineal).
- **Confianza autorreportada:** del padre que pasa de "reflexiono sobre cómo" a "ya sé cómo".
- **Leading indicator de Fase 2:** % de padres que habilitan la billetera del hijo.

---

## Nueva lectura de riesgo

Centrar la Fase 1 en el padre **baja el ROJO 4/4 del PRD original**: sin dinero real del menor, sin PIN bidireccional, sin saldo en tiempo real ni doble actor en esta fase, el riesgo regulatorio, técnico y de usabilidad caen. El reto principal se desplaza a la **calidad del método y el engagement** — no al riesgo financiero. **Dos focos de riesgo propios del nuevo espinazo:** (a) el **motor generativo** (guardrails de Legal arriba) y (b) que el set de features se sienta como un **menú pasivo** si el coach no sostiene la cadencia. Las decisiones bloqueantes de Legal/Ops/Producto se concentran en las features de producto (Metas, Universidad) y se afrontan cuando la demanda ya esté validada.

---

## Qué pasa con lo que ya existe

- **research** (`skandia-kids-research.md`): vigente, con nota de reencuadre Fase 1. Pendiente: profundizar el sprint de "autonomía vs. control".
- **content** (`skandia-kids-content.md`): la voz del método y los **guiones de conversación** (Kiki, provisional) siguen válidos — se reubican dentro de la feature **Planes**. Pendiente: copy de los dos diagnósticos y del resultado generativo.
- **PRD del método** (`skandia-kids-PRD-metodo.md`): ⚠️ **requiere reescritura al nuevo espinazo** — el diagnóstico se parte en dos (padre/hijo), el resultado se vuelve el hub de conciencia, el home pasa a dashboard de 4 features, y la plantilla de etapa ×7 desaparece. El prototipo de Rachel (que muestra "recorrido 7 etapas") queda desactualizado.
- **MVP** (`producto_skandia_kids`): se conserva como **motor de la feature Metas** (fondeo de la billetera, cara del padre).

---

## Principios

1. **El padre es el protagonista — por ahora.** Cada decisión refuerza que el método lo vuelve capaz a él. El hijo entra cuando el padre lo desbloquea.
2. **Acción sobre contenido.** Minutos accionables, no horas de estudio. El baseline del 9% es el recordatorio permanente.
3. **El coach guía, no encierra (híbrido).** Recomienda una acción por semana y prioriza, pero el padre —adulto en su propio portal— nunca queda bloqueado. Fricción suave, no rejas.
4. **El método rompe el tabú.** Las conversaciones son el corazón — porque hablar de plata es lo que el padre no sabe hacer.
5. **Soltar es el objetivo, no controlar.** El método se mide por la *graduación* del hijo a los 18, no por el control parental.
6. **Nada se desperdicia.** La billetera, los cursos y el PRD actual se redespliegan como features y Fase 2.
7. **La personalización es generativa pero acotada.** El LLM redacta; Legal pone los límites. Nunca promete rendimientos ni reemplaza asesoría.

---

*Skandia UX Team · #UXplorers · Junio 2026*
*Ancla para la revisión del experimento Skandia Kids — re-centrado en el padre. Rev. 23 jun: espinazo diagnóstico → conciencia → features.*
