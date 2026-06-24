# PRD Stitch — Skandia Kids
**Adjuntar junto a este archivo:** `skandia-kids-content.md` + `skandia-design-system.md`

---

## Contexto del proyecto

Estoy diseñando **Skandia Kids**, un experimento de educación financiera para adolescentes de 13–17 años con supervisión parental obligatoria. Tiene dos usuarios: el adolescente (protagonista, mobile-first 375px) y el padre/cuidador (supervisor, portal desktop 1280px).

**Restricción de canal:** Skandia Kids **no es una app ni un portal independiente**. El experimento vive dentro de los activos actuales de Skandia: el adolescente accede desde una sección dentro de la **app Skandia existente**, y el padre desde una sección dentro del **portal web Skandia existente**. Todos los diseños deben verse integrados dentro del shell de Skandia — no como producto separado. El usuario no descarga nada nuevo ni crea credenciales nuevas.

Los dos archivos adjuntos son tu fuente de verdad:
- **skandia-kids-content.md** — fuente única de todo el texto de interfaz. No inventes ni parafrasees ningún copy — usa el texto exacto de este archivo según el momento indicado en cada pantalla.
- **skandia-design-system.md** — sistema de diseño Skandia UI Kit v0.1.0. Usa sus tokens de color, tipografía y componentes. No inventes variantes.

---

## Restricciones globales

- Verde principal `#00C73D` — botones primarios, acentos, progreso
- Fondos: tarjetas `#FFFFFF`, página `#F5F5F5`
- Tipografía: Montserrat Bold para títulos · Open Sans para cuerpo · IBM Plex Mono para cifras monetarias
- Sin emojis, sin personajes animados, sin paleta infantil
- Experiencia del adolescente: energética, directa, sin condescendencia — un adolescente de 17 años debe sentirse representado
- Experiencia del padre: idéntica al portal Skandia adulto — sin adaptaciones juveniles
- Máximo 1 botón primario verde por pantalla · Máximo 2 CTAs por pantalla
- Textos legales: al final, 11–12px gris claro, nunca protagonistas
- Bloques naranjas (`#FFF3CD` / borde `#FFA500`): indican contenido pendiente de Legal u Operaciones — deben ser visibles en el diseño

---

## Datos de prueba (usar en todas las pantallas)

- Adolescente: **Valentina**, 16 años
- Padre: **Carlos (papá de Valentina)**
- Nombre del equipo: **Equipo Ramírez**
- Meta activa: **"Mis AirPods"** — $350.000 objetivo · 68% completado · $238.000 acumulados
- Saldo total del billetera: **$412.500**

---

## Pantallas — orden de construcción

---

### Pantalla 01 — Activación parental
**Canvas:** Desktop 1280px · Actor: Padre

Pantalla de onboarding desktop para el padre que activa el espacio financiero de su hijo. Layout de dos columnas: izquierda con texto y CTA, derecha con ilustración placeholder (gradiente verde claro).

Columna izquierda de arriba hacia abajo:
1. Título grande: *usar Momento 1 · Título del content.md*
2. Subtítulo: *usar Momento 1 · Subtítulo*
3. Tres ítems visuales en fila con ícono + texto corto: "El hijo crea metas" / "El padre aprueba movimientos" / "Ambos ven el progreso"
4. Botón primario grande verde ancho completo: *usar Momento 1 · CTA principal*
5. Texto pequeño bajo el botón: *usar Momento 1 · Microcopy bajo CTA*
6. Ícono pregunta verde con tooltip: *usar Momento 1 · Tooltip*
7. Texto legal 11px gris claro al fondo: bloque naranja pendiente legal

Tono: confiable, adulto, control visible. El padre siente seguridad.

---

### Pantalla 02 — Bienvenida del adolescente
**Canvas:** Mobile 375px · Actor: Adolescente

Primera pantalla que ve el adolescente. Layout en columna: visual superior (placeholder gradiente verde claro a blanco, 220px altura) + contenido inferior.

Contenido de arriba hacia abajo:
1. Visual abstracto/geométrico — energético, no infantil (placeholder verde claro)
2. Título grande: *usar Momento 2 · Título*
3. Subtítulo: *usar Momento 2 · Subtítulo*
4. Botón primario ancho completo: *usar Momento 2 · CTA principal*
5. Texto pequeño gris: *usar Momento 2 · Microcopy*
6. Texto link gris: *usar Momento 2 · Mensaje secundario*

El título es el elemento más importante — el adolescente debe sentir que esto es SUYO. Directo, sin tono de banco tradicional.

---

### Pantalla 03 — Armar el equipo
**Canvas:** Mobile 375px · Actor: Adolescente

Segunda pantalla del onboarding. Sin visual decorativo — empieza directo con el contenido.

Contenido de arriba hacia abajo:
1. Título: "Tu equipo ya está listo."
2. Subtítulo gris: "Aquí están las personas que te acompañan. Cuando haya movimientos de plata, ellos dan el visto bueno."
3. Tarjeta miembro 1: avatar circular inicial "C" · "Carlos (papá)" · badge gris "Tu equipo"
4. Tarjeta miembro 2: logo Skandia · "Skandia" · chip verde "Coach financiero"
5. Campo de texto: label "Dale un nombre a tu equipo (opcional)" · placeholder "Equipo García, Los Romero, el nombre que quieras..." · valor sugerido pre-llenado: "Equipo Ramírez"
6. Botón primario ancho completo: "Empezar con mi equipo"

Tarjetas con borde gris claro, esquinas 12px. Chip "Coach financiero" en verde claro con texto verde.

---

### Pantalla 04 — Dashboard del adolescente
**Canvas:** Mobile 375px · Actor: Adolescente

Pantalla principal — hub central. Header fijo + scroll vertical.

**Header fijo:** logo Skandia izquierda · chip "Equipo Ramírez" centro · avatar "V" derecha

**Sección saldo (primer elemento, más prominente):**
- Label pequeño gris: "Tu plata ahora"
- Cifra grande monoespaciada: **$412.500**
- Barra skeleton gris muy fina debajo (simula actualización en tiempo real)

**Sección meta activa:**
- Tarjeta blanca con borde izquierdo verde 4px
- "Mis AirPods" · barra de progreso verde 68% · "$238.000 de $350.000" · chip "En progreso"

**Sección reto desbloqueado:**
- Tarjeta fondo verde muy claro
- Badge verde: "Reto desbloqueado"
- Texto: "¿Sabes en qué se va tu plata cada semana?"
- Botón secundario pequeño: "Ver reto"

**Sección Tu zona de aprendizaje (scroll horizontal):**
- Título de sección 14px bold oscuro: "Tu zona de aprendizaje"
- Fila de 3 tarjetas en scroll horizontal (`overflow-x: auto`). Cada tarjeta: 150×180px, `border-radius: 12px`, `padding: 16px`

  **Tarjeta 1 — Nivel 1 (activa):**
  - Fondo gradiente diagonal `#003d1a` → `#00c73d`
  - Badge "Nivel 1" blanco (arriba izquierda)
  - Ícono alcancía blanco 28px centrado
  - Título blanco bold 13px: "¿Para qué sirve ahorrar?"
  - Barra de progreso blanca semitransparente: 0% relleno

  **Tarjeta 2 — bloqueada:**
  - Fondo gris `#e8e8e8`, `opacity: 0.5`
  - Ícono candado gris 28px · Título gris 13px: "La magia del interés"
  - Texto 11px: "Completa el nivel 1"

  **Tarjeta 3 — bloqueada:**
  - Mismo estilo que tarjeta 2
  - Ícono gráfico de línea gris · Título gris 13px: "Gastos que no ves"

**Acciones rápidas (fila):** "Nueva meta" · "Sumar plata" · "Retirar" — botones secundarios

Fondo general `#F5F5F5`. Tarjetas blancas con sombra suave. La cifra del saldo es el elemento visual más importante.

---

### Pantalla 05 — Crear meta
**Canvas:** Mobile 375px · Actor: Adolescente

Formulario de creación de meta. Header con flecha atrás. CTA fijo al fondo.

Contenido:
1. Título-pregunta grande: *usar Momento 3 · Título*
2. Campo texto sin label — solo placeholder: *usar Momento 3 · Placeholder*
3. Campo monto con prefijo "$": label *usar Momento 3 · Label monto*
4. Campo fecha: label *usar Momento 3 · Label fecha*
5. Checkbox: "Sin fecha por ahora"

CTA fijo al fondo: *usar Momento 3 · CTA*

Campos con mucho espacio — no apretados. Al enfocar, borde verde. El prefijo "$" en gris dentro del campo de monto.

---

### Pantalla 06A — Solicitar aporte (vista adolescente)
**Canvas:** Mobile 375px · Actor: Adolescente

Pantalla simple de solicitud. CTA fijo al fondo.

Contenido:
1. Título: *usar Momento 4A · Título (vista adolescente)*
2. Subtítulo gris: *usar Momento 4A · Subtítulo*
3. Campo monto grande prominente: label "Monto a sumar" · placeholder "$0" · cifra 24px
4. Selector opcional gris claro: "Asociar a una meta (opcional)" · opción: "Mis AirPods"

CTA fijo: *usar Momento 4A · CTA*

Toast verde al enviar: *usar Momento 4A · Confirmación adolescente*

---

### Pantalla 06B — Validación PIN del padre (aporte)
**Canvas:** Desktop — modal 480px centrado · Actor: Padre

Modal sobre el dashboard del padre. Fondo oscurecido detrás.

Contenido del modal:
1. Ícono notificación verde centrado (campana)
2. Título: "Valentina quiere sumar $120.000 a su billetera"
3. Subtítulo gris: "El dinero saldría de tu cuenta [Cuenta vinculada Skandia]."
4. Campo PIN: 6 puntos/círculos enmascarados centrados · label "Ingresa tu PIN"
5. Botón primario: *usar Momento 4A · CTA principal (vista padre)*
6. Botón secundario outlined: *usar Momento 4A · CTA secundario*
7. Bloque naranja pendiente al fondo: "⚠️ PENDIENTE LEGAL: aviso legal obligatorio — no publicar sin validación."

Modal fondo blanco, `border-radius: 16px`, sombra `0 8px 32px rgba(0,0,0,0.15)`.

---

### Pantalla 07 — Aporte directo del padre
**Canvas:** Desktop 1280px · Actor: Padre

Formulario centrado (max 600px) sobre fondo gris claro. Tarjeta blanca con el contenido.

Contenido de la tarjeta:
1. Título: *usar Momento 4B · Título*
2. Subtítulo: *usar Momento 4B · Subtítulo*
3. Campo monto: label "Monto a sumar" · prefijo "$" · cifra grande
4. Selector cuenta origen: "Cuenta de ahorro Skandia ••••4821"
5. Separador línea gris
6. Campo PIN: 6 puntos centrados · label "Confirma con tu PIN"
7. Botón primario ancho completo: *usar Momento 4B · CTA*
8. Bloque naranja pendiente: "⚠️ PENDIENTE LEGAL"

Estado de éxito (mismo espacio tras confirmar): ícono check verde 48px · *usar Momento 4B · Toast padre* · mensaje info azul · botón secundario "Volver al portal"

---

### Pantalla 08A — Solicitar retiro (vista adolescente)
**Canvas:** Mobile 375px · Actor: Adolescente

Igual en estructura a la pantalla 06A pero para retiro.

Contenido:
1. Título: *usar Momento 4C · Título*
2. Subtítulo: *usar Momento 4C · Subtítulo*
3. Campo monto: label "Monto a retirar" · placeholder "$0"
4. Texto referencia gris bajo el campo: "Disponible: $412.500"

CTA fijo: *usar Momento 4C · CTA adolescente*

Toast info al enviar: *usar Momento 4C · Confirmación adolescente*

---

### Pantalla 08B — Validación PIN del padre (retiro)
**Canvas:** Desktop — modal 480px centrado · Actor: Padre

Igual en estructura a 06B pero para retiro. El ícono es naranja (flecha saliendo) para diferenciar visualmente del aporte.

Contenido:
1. Ícono naranja de retiro centrado
2. Título: *usar Momento 4C · Título notificación padre*
3. Campo PIN: 6 puntos
4. Botón primario: *usar Momento 4C · CTA del padre*
5. **Bloque naranja pendiente (operaciones):** "⚠️ PENDIENTE OPERACIONES: plazo de retiro en días hábiles — dato real requerido antes de producción."
6. Bloque naranja pendiente (legal): aviso legal pendiente

---

### Pantalla 09 — Meta cumplida
**Canvas:** Mobile 375px · Actor: Adolescente

Pantalla de celebración. Parte superior 55%: celebración visual. Parte inferior: acciones.

**Parte superior:**
- Gradiente fondo: blanco a verde clarísimo `#E8F8ED`
- Insignia 80px: círculo verde · ícono trofeo blanco · sombra verde suave
- Badge: "Meta cumplida" fondo `#E8F8ED` texto `#00703A`
- Título verde: *usar Momento 5 · Título*
- Subtítulo: *usar Momento 5 · Subtítulo*

**Parte inferior:**
1. Botón primario: *usar Momento 5 · CTA principal*
2. Botón secundario outlined: *usar Momento 5 · CTA secundario*
3. Link texto verde: "Hacer crecer esta plata →"
4. Microcopy gris bajo "Retirar": *usar Momento 5 · Microcopy*

Energético pero sobrio — un adolescente de 17 años debe querer compartir esta pantalla.

---

### Pantalla 10 — Hacer crecer
**Canvas:** Mobile 375px · Actor: Adolescente

Pantalla educativa sobre inversión. Scroll suave. CTA al fondo.

Contenido de arriba hacia abajo:
1. Chip verde claro: ícono Skandia + "Coach Skandia"
2. Visual comparativo en tarjeta dividida en dos mitades:
   - Izquierda fondo gris: ícono alcancía · "Guardar" · "Tu plata espera quieta"
   - Derecha fondo verde claro: ícono planta/flecha arriba · "Hacer crecer" · "Tu plata trabaja sola"
3. Título: *usar Momento 6 · Título*
4. Subtítulo: *usar Momento 6 · Subtítulo*
5. Acordeón colapsado: "¿Y si baja? +" — al expandir: *usar Momento 6 · Explicación capa 2*
6. Microcopy gris: *usar Momento 6 · Microcopy*
7. **Bloque naranja pendiente:** "⚠️ PENDIENTE LEGAL + PRODUCTO: copy de riesgo exacto pendiente. No publicar sin validación."

CTA al fondo: *usar Momento 6 · CTA* · Link gris: "Ahora no"

---

### Pantalla 11 — Reto desbloqueado
**Canvas:** Mobile 375px — bottom sheet sobre dashboard · Actor: Adolescente

Modal tipo hoja inferior (bottom sheet). Ocupa 70% de pantalla. Esquinas superiores redondeadas. Fondo oscurecido arriba.

Contenido del sheet:
1. Pill de agarre gris centrado (4×32px)
2. Badge verde grande centrado: ícono candado abierto + "Reto desbloqueado"
3. Tarjeta fondo gris claro con descripción: *usar Momento 8 · Descripción del reto*
4. Chip con estrella: *usar Momento 8 · Recompensa visible*
5. Microcopy privacidad 11px gris: *usar Momento 8 · Microcopy*
6. Botón primario ancho completo: *usar Momento 8 · CTA*
7. Link texto gris centrado: *usar Momento 8 · Opción secundaria*

---

### Pantalla 12 — Dashboard parental
**Canvas:** Desktop 1280px · Actor: Padre

Portal web adulto. Sidebar izquierda (240px) + área de contenido.

**Sidebar:** Logo Skandia · nav: Inicio / Mi portafolio / **Skandia Kids ✦** (activo) / Configuración · avatar "Carlos" al fondo

**Área de contenido:**

Alerta acción pendiente (banner amarillo, borde izquierdo naranja 4px):
- Ícono campana naranja · *usar Momento 7 · Alerta de solicitud pendiente* · botón secundario "Ver solicitud"

Cabecera de sección:
- Título H2: *usar Momento 7 · Título sección*
- Subtítulo: *usar Momento 7 · Subtítulo*
- Botón primario derecha: *usar Momento 7 · CTA acceso al canal*

Tarjeta meta activa: "Mis AirPods" · barra progreso verde 68% · "$238.000 de $350.000" · tag "En progreso"

Mensaje tranquilidad (si no hay alerta): caja info azul claro · *usar Momento 7 · Mensaje si no hay actividad reciente*

Tono idéntico al portal Skandia adulto — sin ningún elemento de la app del adolescente.

---

### Pantalla 13 — Lección 1: ¿Para qué sirve ahorrar?
**Canvas:** Mobile 375px · Actor: Adolescente

Pantalla de microlección. Accesible desde la tarjeta "Nivel 1" en el dashboard. Tono: coach que habla de igual a igual — no profesor.

**Header fijo:**
- Flecha atrás (vuelve al dashboard)
- Título centrado: "Nivel 1"
- Badge verde claro derecha: "En progreso"

**Barra de pasos (debajo del header, fija):**
- 4 círculos conectados por línea: paso 1 verde relleno · pasos 2–3–4 gris vacío
- Texto: "Paso 1 de 4" gris 12px

**Tarjeta de concepto (scroll):**
- Ilustración placeholder: rectángulo `#E8F8ED`, 100% ancho, 140px alto, ícono alcancía verde 48px centrado
- Título H2: "¿Para qué sirve ahorrar?"
- Cuerpo 16px: "Ahorrar no es solo guardar plata para no gastarla. Es separar una parte de lo que tienes ahora para lograr algo que quieres más adelante. Cada peso que guardas hoy es un paso hacia tu próxima meta."

**Pregunta de verificación (misma tarjeta, con divisor):**
- Título 16px bold: "¿Cuál de estas es la mejor razón para ahorrar?"
- 3 radio-cards con borde gris 1px, `border-radius: 8px`:
  1. "Para no gastar todo de una vez"
  2. "Para lograr algo que quiero" ← **correcta**
  3. "Porque mis papás me lo dijeron"
- Estado activo: borde verde 2px + check verde
- **Feedback correcto:** caja `#E8F8ED`, ícono check verde, texto: "¡Exacto! Ahorrar con propósito es más poderoso que ahorrar sin meta."
- **Feedback incorrecto:** caja `#F5F5F5`, texto gris: "Casi — piénsalo de nuevo. ¿Cuál tiene más que ver con tus metas?"

**CTA fijo al fondo (visible solo tras acierto):**
- Botón primario verde: "Siguiente →"
- Al presionar: toast "Paso 1 completado · +10 puntos" → regresa al dashboard con barra de Nivel 1 en 25%

---

*Skandia UX Team · UXplorers Agents · Junio 2026*
