# PRD Stitch — Skandia Kids · Flujo del Adolescente
**Adjuntar junto a este archivo:** `skandia-design-system.md`
**Versión:** Standalone — copy ya incluido, no requiere content.md

---

## Quién es este usuario

**Valentina, 16 años.** Usa su celular todo el día. Tiene metas a corto plazo y tangibles (tenis, viaje, concierto). Ve el ahorro como "guardar para luego gastar". Confunde inversión con ahorro — los conceptos no están formados porque nunca ha tenido un contexto práctico donde aprenderlos.

**Lo que necesita sentir en cada pantalla:**
- Esto es MÍO — no es una cuenta de mis papás con mi nombre
- Entiendo lo que está pasando con mi plata, sin que me lo expliquen como a un niño
- Puedo hacer cosas reales aquí, no solo "ver"
- Aprender no se siente como clase — se siente como subir de nivel

**Lo que NO debe sentir:**
- Que le están pidiendo permiso a sus papás (aunque técnicamente sí)
- Que está en una app de banco aburrida para adultos
- Que la supervisión parental es un bloqueo — es parte del proceso
- Que lo están tratando como niño de 8 años

---

## Restricciones globales

- **Canal:** App Skandia existente — no es una app independiente. Valentina accede desde una sección dentro de la app Skandia que su familia ya usa.
- **Canvas:** Mobile 375px — todas las pantallas son mobile first
- Verde principal `#00C73D` — botones primarios, acentos, progreso
- Fondos: tarjetas `#FFFFFF`, página `#F5F5F5`
- Tipografía: Montserrat Bold para títulos · Open Sans para cuerpo · IBM Plex Mono para cifras monetarias
- **Sin emojis, sin personajes animados, sin paleta infantil** — un adolescente de 17 años debe sentirse representado
- Máximo 1 botón primario verde por pantalla · Máximo 2 CTAs por pantalla
- La gamificación vive en la mecánica (niveles, retos, progreso), no en el tono — no todo necesita exclamación
- Textos legales: al final, 11–12px gris claro, nunca protagonistas

---

## Datos de prueba

- Adolescente: **Valentina**, 16 años
- Padre: **Carlos (papá)**
- Nombre del equipo: **Equipo Ramírez**
- Meta activa: **"Mis AirPods"** — $350.000 objetivo · 68% completado · $238.000 acumulados
- Saldo billetera: **$412.500**

---

## Pantallas — orden de construcción

---

### Pantalla 02 — Bienvenida del adolescente
**Canvas:** Mobile 375px
**Momento:** Primera pantalla que ve Valentina — debe convencerla en 3 segundos de que esto no es una app de banco aburrida

Layout en columna: visual superior 220px + contenido inferior con scroll.

**Visual superior (220px):**
- Placeholder: gradiente diagonal verde oscuro `#003d1a` → verde claro `#00C73D`
- Forma geométrica abstracta (no infantil) — líneas o bloques angulares, sin personajes

**Contenido inferior — de arriba hacia abajo:**

1. **Título H1** (Montserrat Bold 32px, color oscuro `#1a1a1a`):
   "Esta es tu plata. Aquí decides qué hacer con ella."

2. **Subtítulo** (Open Sans 16px, gris `#666666`, interlineado 1.5):
   "Puedes crear metas, ver cómo crece tu dinero y aprender cómo funcionan las inversiones — practicando de verdad."

3. **Botón primario** verde, ancho completo, altura 52px:
   "Crear mi primera meta"

4. **Microcopy** (Open Sans 13px, gris, centrado):
   "Para mover plata, tu equipo da el visto bueno. Tú pones la dirección."

5. **Texto link** (gris, centrado, 14px):
   "¿Para qué quieres guardar tu plata? Eso lo decides tú."

**Tono:** El título es el elemento más importante — Valentina debe sentir que esto es SUYO desde la primera línea.

---

### Pantalla 03 — Armar el equipo
**Canvas:** Mobile 375px
**Momento:** Onboarding paso 2 — Valentina conoce a los miembros de su equipo y le da nombre

Sin visual decorativo — empieza directo con el contenido.

**Contenido — de arriba hacia abajo:**

1. **Título H2** (Montserrat Bold 26px):
   "Tu equipo ya está listo."

2. **Subtítulo** (Open Sans 15px, gris):
   "Aquí están las personas que te acompañan. Cuando haya movimientos de plata, ellos dan el visto bueno."

3. **Tarjeta miembro 1** (fondo blanco, borde gris claro 1px, `border-radius: 12px`, padding 16px):
   - Avatar circular inicial "C" (fondo verde claro, letra verde)
   - Texto bold: "Carlos (papá)"
   - Badge gris pequeño: "Tu equipo"

4. **Tarjeta miembro 2** (mismo estilo):
   - Logo Skandia pequeño (en lugar de avatar)
   - Texto bold: "Skandia"
   - Chip verde claro, texto verde: "Coach financiero"

5. **Campo de texto:**
   - Label (14px, gris): "Dale un nombre a tu equipo (opcional)"
   - Placeholder: "Equipo García, Los Romero, el nombre que quieras..."
   - Valor pre-llenado sugerido: "Equipo Ramírez"
   - Borde gris → borde verde al enfocar

6. **Botón primario** verde, ancho completo:
   "Empezar con mi equipo"

---

### Pantalla 04 — Dashboard de Valentina
**Canvas:** Mobile 375px
**Momento:** Pantalla principal — lo que ve cada vez que abre la app

Layout: Header fijo + scroll vertical. Secciones diferenciadas con espaciado generoso.

**Header fijo** (fondo blanco, sombra `0 2px 4px rgba(0,0,0,0.06)`):
- Logo Skandia (izquierda, pequeño)
- Chip "Equipo Ramírez" (centro, fondo verde claro `#E8F8ED`, texto verde `#00703A`)
- Avatar circular "V" (derecha, fondo verde, letra blanca)

**Sección 1 — Saldo** (primera, la más prominente):
- Label 13px gris: "Tu plata ahora"
- Cifra IBM Plex Mono Bold 38px color `#1a1a1a`: **$412.500**
- Barra skeleton gris muy fina debajo (1px, simula actualización en tiempo real)

**Sección 2 — Meta activa:**
- Tarjeta blanca, `border-radius: 12px`, sombra suave, borde izquierdo 4px verde
- Nombre: "Mis AirPods" (bold 16px)
- Barra de progreso: relleno verde 68%, fondo `#E8F8ED`, altura 8px, `border-radius: 4px`
- Texto 14px gris: "$238.000 de $350.000"
- Chip verde claro: "En progreso"

**Sección 3 — Reto desbloqueado:**
- Tarjeta fondo verde muy claro `#E8F8ED`, `border-radius: 12px`, padding 16px
- Badge verde `#00C73D`: "Reto desbloqueado"
- Texto 15px: "¿Sabes en qué se va tu plata cada semana?"
- Botón secundario pequeño (borde verde, texto verde): "Ver reto"

**Sección 4 — Tu zona de aprendizaje:**
- Título 14px bold oscuro: "Tu zona de aprendizaje"
- Fila de 3 tarjetas en scroll horizontal. Cada tarjeta: 150×180px, `border-radius: 12px`, `padding: 16px`, `flex-shrink: 0`

  **Tarjeta 1 — Nivel 1 (activa):**
  - Fondo gradiente diagonal `#003d1a` → `#00c73d`
  - Badge "Nivel 1" blanco pequeño (arriba izquierda)
  - Ícono alcancía blanco 28px centrado
  - Título blanco bold 13px: "¿Para qué sirve ahorrar?"
  - Barra de progreso blanca semitransparente: 0% relleno

  **Tarjeta 2 — bloqueada:**
  - Fondo gris `#e8e8e8`, `opacity: 0.5`
  - Ícono candado gris 28px
  - Título gris 13px: "La magia del interés"
  - Texto 11px: "Completa el nivel 1"

  **Tarjeta 3 — bloqueada:**
  - Mismo estilo que tarjeta 2
  - Ícono gráfico de línea gris
  - Título gris 13px: "Gastos que no ves"

**Sección 5 — Acciones rápidas** (fila de botones secundarios, borde gris):
- "Nueva meta" · "Sumar plata" · "Retirar"

---

### Pantalla 05 — Crear meta
**Canvas:** Mobile 375px
**Momento:** Valentina define qué quiere lograr con su plata

Header con flecha atrás. CTA fijo al fondo. Campos con mucho espacio — no apretados.

**Contenido — de arriba hacia abajo:**

1. **Título H2** (Montserrat Bold 28px):
   "¿Para qué quieres guardar?"

2. **Campo texto** (sin label — solo placeholder):
   - Placeholder gris: "Ej: mis tenis, viaje a Santa Marta, mi primer millón"
   - Borde gris → borde verde al enfocar

3. **Campo monto:**
   - Label 14px gris: "¿Cuánto necesitas?"
   - Prefijo "$" gris dentro del campo
   - Cifra IBM Plex Mono 20px
   - Borde gris → borde verde al enfocar

4. **Campo fecha:**
   - Label 14px gris: "¿Para cuándo?"
   - Selector de fecha estándar

5. **Checkbox** (fila): cuadro + texto 14px gris: "Sin fecha por ahora"

**CTA fijo al fondo:**
- Botón primario verde, ancho completo: "Crear esta meta"

**Microcopy de confirmación** (aparece tras crear):
- Toast verde: "Meta creada. Tu equipo ya la puede ver."

---

### Pantalla 06A — Solicitar aporte
**Canvas:** Mobile 375px
**Momento:** Valentina quiere que le sumen plata a su billetera — no se siente como pedir permiso, es completar un paso

Header con flecha atrás. CTA fijo al fondo.

**Contenido — de arriba hacia abajo:**

1. **Título H2** (Montserrat Bold 26px):
   "¿Cuánto quieres sumar a tu billetera?"

2. **Subtítulo** (Open Sans 15px, gris):
   "Tu familia recibirá una notificación para confirmar el traslado."

3. **Campo monto** (prominente):
   - Label 14px: "Monto a sumar"
   - Cifra IBM Plex Mono 24px, centrada
   - Placeholder: "$0"
   - Borde gris → borde verde al enfocar

4. **Selector opcional** (fondo gris claro, `border-radius: 8px`, padding 12px):
   - Texto 14px gris: "Asociar a una meta (opcional)"
   - Dropdown: "Mis AirPods"

**CTA fijo al fondo:**
- Botón primario verde, ancho completo: "Solicitar aporte"

**Toast** (al enviar):
- Fondo verde claro `#E8F8ED`, texto verde oscuro: "Solicitud enviada. Cuando tu familia lo confirme con su PIN, el dinero llega a tu billetera."

---

### Pantalla 08A — Solicitar retiro
**Canvas:** Mobile 375px
**Momento:** Valentina quiere retirar plata de su billetera — mismo tono que el aporte, no es pedir permiso

Header con flecha atrás. CTA fijo al fondo.

**Contenido — de arriba hacia abajo:**

1. **Título H2** (Montserrat Bold 26px):
   "¿Cuánto quieres retirar?"

2. **Subtítulo** (Open Sans 15px, gris):
   "Tu familia confirma el retiro con su PIN. El dinero llega a [destino definido]."

3. **Campo monto:**
   - Label 14px: "Monto a retirar"
   - Cifra IBM Plex Mono 24px, centrada
   - Placeholder: "$0"
   - Borde gris → borde verde al enfocar

4. **Referencia disponible** (texto 13px gris, bajo el campo):
   "Disponible: $412.500"

**CTA fijo al fondo:**
- Botón primario verde, ancho completo: "Solicitar retiro"

**Toast** (al enviar):
- Fondo `#E8F3FF`, texto azul oscuro: "Solicitud lista. Cuando tu familia confirme con PIN, el dinero se procesa."

---

### Pantalla 09 — Meta cumplida
**Canvas:** Mobile 375px
**Momento:** Valentina llegó a su meta — celebración que no sobreactúa

Layout dividido: parte superior 55% celebración visual + parte inferior acciones.

**Parte superior** (gradiente blanco → verde clarísimo `#E8F8ED`):
- Insignia 80px centrada: círculo verde `#00C73D`, ícono trofeo blanco, sombra verde suave
- Badge "Meta cumplida" (fondo `#E8F8ED`, texto verde oscuro `#00703A`, `border-radius: 20px`)
- Título (Montserrat Bold 28px, verde `#00703A`): "¡Lo lograste!"
- Subtítulo (Open Sans 16px, gris): "Llegaste a tu meta 'Mis AirPods'. ¿Qué quieres hacer con esta plata?"

**Parte inferior:**

1. **Botón primario** verde, ancho completo: "Retirar"

2. **Botón secundario** outlined (borde verde, texto verde), ancho completo: "Crear una nueva meta"

3. **Link texto** verde, centrado: "Hacer crecer esta plata →"

4. **Microcopy** bajo "Retirar" (13px gris centrado):
   "Para retirar, tu equipo recibirá una notificación para aprobarlo."

**Tono:** Energético pero sobrio — un adolescente de 17 años debe querer compartir esta pantalla.

---

### Pantalla 10 — Hacer crecer
**Canvas:** Mobile 375px
**Momento:** Primera vez que Valentina escucha sobre inversión — sin clase magistral

Scroll suave. CTA fijo al fondo.

**Contenido — de arriba hacia abajo:**

1. **Chip Coach** (fondo verde claro, texto verde, `border-radius: 20px`):
   Ícono Skandia pequeño + "Coach Skandia"

2. **Tarjeta comparativa** (dividida en 2 mitades, `border-radius: 12px`):
   - **Izquierda** (fondo gris `#F5F5F5`):
     Ícono alcancía gris 28px · "Guardar" (bold 14px) · "Tu plata espera quieta" (13px gris)
   - **Derecha** (fondo verde claro `#E8F8ED`):
     Ícono planta/flecha arriba verde 28px · "Hacer crecer" (bold 14px, verde) · "Tu plata trabaja sola" (13px verde oscuro)

3. **Título H2** (Montserrat Bold 24px):
   "Tu plata puede hacer más que esperar."

4. **Subtítulo** (Open Sans 16px, gris, interlineado 1.5):
   "Cuando guardas en una meta normal, tu plata espera quieta. Cuando eliges hacerla crecer, trabaja mientras tú haces otras cosas."

5. **Acordeón colapsado** (fondo gris claro, `border-radius: 8px`, padding 14px):
   - Título visible: "¿Y si baja? +" (14px, toque en fila derecha para expandir)
   - Contenido al expandir: "No es magia ni es seguro al 100%. A veces sube, a veces baja un poco. Pero con tiempo, tiende a crecer."

6. **Microcopy** (13px gris centrado):
   "Cualquier cambio lo aprueba tu equipo."

7. **Bloque naranja** (fondo `#FFF3CD`, borde `1px solid #FFA500`, `border-radius: 8px`, padding 12px):
   "⚠️ PENDIENTE LEGAL + PRODUCTO: copy de riesgo exacto pendiente. No publicar sin validación."

**CTA fijo al fondo:**
- Botón primario verde, ancho completo: "Explorar esta opción"
- Link gris centrado debajo: "Ahora no"

---

### Pantalla 11 — Reto desbloqueado
**Canvas:** Mobile 375px — bottom sheet sobre el dashboard
**Momento:** Valentina desbloquea su primer microreto de aprendizaje

Modal tipo hoja inferior (bottom sheet). Ocupa 70% de la pantalla. Esquinas superiores redondeadas (`border-radius: 20px 20px 0 0`). Fondo oscurecido arriba (`rgba(0,0,0,0.4)`).

**Contenido del sheet — de arriba hacia abajo:**

1. **Pill de agarre** (4×32px, fondo gris `#D0D0D0`, `border-radius: 2px`, centrado, margin top 12px)

2. **Badge** (fondo verde `#00C73D`, texto blanco, `border-radius: 20px`, padding 8px 16px, centrado):
   Ícono candado abierto + "Reto desbloqueado"

3. **Tarjeta reto** (fondo gris claro `#F5F5F5`, `border-radius: 12px`, padding 16px):
   Texto 15px oscuro: "¿Sabes en qué se va tu plata cada semana? Registra tus 3 gastos más grandes de los últimos 7 días."

4. **Chip recompensa** (fila centrada):
   Ícono estrella verde + texto 14px verde: "Completa este reto y desbloquea el siguiente nivel"

5. **Microcopy privacidad** (11px gris, centrado):
   "Este reto es solo tuyo. No se comparte con tu equipo."

6. **Botón primario** verde, ancho completo: "Empezar reto"

7. **Link texto** gris centrado 14px: "Más tarde"

---

### Pantalla 13 — Lección 1: ¿Para qué sirve ahorrar?
**Canvas:** Mobile 375px
**Momento:** Valentina entra al contenido educativo desde "Tu zona de aprendizaje" en el dashboard

Header fijo. Barra de pasos fija. CTA fijo al fondo (oculto hasta que acierta la pregunta).

**Header fijo** (fondo blanco, sombra sutil):
- Flecha atrás izquierda (vuelve al dashboard)
- Título centrado: "Nivel 1" (Montserrat Bold 16px)
- Badge derecha (fondo verde claro, texto verde): "En progreso"

**Barra de pasos** (debajo del header, fija):
- 4 círculos conectados por línea horizontal:
  - Paso 1: relleno verde `#00C73D`
  - Pasos 2–3–4: vacíos, borde gris `#D0D0D0`
- Texto 12px gris centrado: "Paso 1 de 4"

**Tarjeta de concepto** (scroll, fondo blanco, `border-radius: 12px`, sombra suave, padding 24px):

Ilustración placeholder (rectángulo fondo `#E8F8ED`, 100% ancho, 140px alto, ícono alcancía verde 48px centrado)

Título H2 24px bold: "¿Para qué sirve ahorrar?"

Cuerpo Open Sans 16px, interlineado 1.6, color `#333333`:
"Ahorrar no es solo guardar plata para no gastarla. Es separar una parte de lo que tienes ahora para lograr algo que quieres más adelante. Cada peso que guardas hoy es un paso hacia tu próxima meta."

**Divisor** línea gris claro

**Pregunta de verificación:**

Título 16px bold: "¿Cuál de estas es la mejor razón para ahorrar?"

3 opciones como radio-cards (borde gris 1px, `border-radius: 8px`, padding 14px, ancho completo):
1. "Para no gastar todo de una vez"
2. "Para lograr algo que quiero" ← **respuesta correcta**
3. "Porque mis papás me lo dijeron"

Estado seleccionado: borde verde 2px + ícono check verde derecha

**Feedback correcto** (caja `#E8F8ED`, `border-radius: 8px`, padding 12px, ícono check verde):
"¡Exacto! Ahorrar con propósito es más poderoso que ahorrar sin meta."

**Feedback incorrecto** (caja `#F5F5F5`, `border-radius: 8px`, padding 12px, ícono info gris):
"Casi — piénsalo de nuevo. ¿Cuál tiene más que ver con tus metas?"

**CTA fijo al fondo** (visible solo tras acierto):
- Botón primario verde ancho completo: "Siguiente →"
- Al presionar: toast verde "Paso 1 completado · +10 puntos" → regresa al dashboard con barra de Nivel 1 al 25%

---

## Conexión entre pantallas

```
P02 (Bienvenida)
  └─→ P03 (Armar equipo)
        └─→ P04 (Dashboard) ←─ punto de entrada habitual
              ├─→ P05 (Crear meta)
              ├─→ P06A (Solicitar aporte)
              ├─→ P08A (Solicitar retiro)
              ├─→ P11 (Reto desbloqueado — bottom sheet sobre P04)
              └─→ P13 (Lección 1 — desde zona de aprendizaje)
                    └─→ P04 (regresa al completar)

P09 (Meta cumplida) ←─ se activa cuando progreso llega al 100%
  └─→ P10 (Hacer crecer) ←─ accesible desde link en P09
```

Los modales y bottom sheets (P11) aparecen sobre el dashboard — Valentina no pierde el contexto de dónde está.

---

*Skandia UX Team · UXplorers Agents · Junio 2026*
