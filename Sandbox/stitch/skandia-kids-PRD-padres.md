# PRD Stitch — Skandia Kids · Flujo del Padre
**Adjuntar junto a este archivo:** `skandia-design-system.md`
**Versión:** Standalone — copy ya incluido, no requiere content.md

---

## Quién es este usuario

**Carlos, papá de Valentina (16 años).** Tiene un producto activo en Skandia. No es el protagonista de la experiencia — es el habilitador y el supervisor. Su motivación: que su hija aprenda a manejar dinero ahora, antes de llegar a la universidad.

**Lo que necesita sentir en cada pantalla:**
- Tiene el control total de lo que se mueve
- Ve todo lo que pasa sin tener que preguntar
- El entorno es confiable — es Skandia, no una app desconocida
- No tiene que aprender nada nuevo — funciona igual que el portal que ya conoce

**Lo que NO debe sentir:**
- Que está cediendo el control de su dinero
- Que tiene que aprobar cada micro-decisión de su hija (solo las transacciones)
- Que el portal cambió de look — debe verse idéntico al portal Skandia adulto

---

## Restricciones globales

- **Canal:** Portal web Skandia existente — no es una app ni un portal independiente. El padre accede desde una sección dentro del portal que ya usa.
- Verde principal `#00C73D` — botones primarios, acentos, progreso
- Fondos: tarjetas `#FFFFFF`, página `#F5F5F5`
- Tipografía: Montserrat Bold para títulos · Open Sans para cuerpo · IBM Plex Mono para cifras
- **Tono idéntico al portal Skandia adulto** — sin adaptaciones juveniles, sin íconos lúdicos, sin paleta de colores del flujo adolescente
- Máximo 1 botón primario verde por pantalla · Máximo 2 CTAs por pantalla
- Textos legales: al final, 11–12px gris claro, nunca protagonistas
- Bloques naranjas (`#FFF3CD` / borde `#FFA500`): pendientes de Legal u Operaciones — deben ser visibles

---

## Datos de prueba

- Padre: **Carlos (papá de Valentina)**
- Adolescente: **Valentina**, 16 años
- Nombre del equipo: **Equipo Ramírez**
- Meta activa de Valentina: **"Mis AirPods"** — $350.000 objetivo · 68% completado · $238.000 acumulados
- Saldo billetera de Valentina: **$412.500**
- Cuenta vinculada: **Cuenta de ahorro Skandia ••••4821**

---

## Pantallas — orden de construcción

---

### Pantalla 01 — Activación parental
**Canvas:** Desktop 1280px
**Momento:** Primera vez — el padre activa la billetera de su hija desde el portal

Layout de dos columnas. Columna izquierda: texto + CTA. Columna derecha: ilustración placeholder (gradiente verde claro, abstracto, no infantil).

**Columna izquierda — de arriba hacia abajo:**

1. **Título H1** (Montserrat Bold, 36px):
   "Tu hijo aprende a manejar su plata. Tú siempre sabes cómo va."

2. **Subtítulo** (Open Sans, 18px, gris oscuro):
   "Skandia Kids es un espacio donde tu hijo practica con dinero real, con metas que él elige y movimientos que tú apruebas."

3. **Tres ítems en fila** (ícono + texto corto, separados con divisor vertical):
   - Ícono meta/bandera → "El hijo crea metas"
   - Ícono campana → "El padre aprueba movimientos"
   - Ícono gráfico de progreso → "Ambos ven el avance"

4. **Botón primario** verde, ancho completo, altura 52px:
   "Activar para mi hijo/hija"

5. **Microcopy** bajo el botón (Open Sans 14px, gris):
   "Tú controlas cada movimiento. Tu hijo tiene la experiencia."

6. **Ícono pregunta** verde con tooltip al pasar:
   Tooltip: "¿Cómo funciona la aprobación? Cada vez que tu hijo quiera mover plata, te llegará una notificación para que tú apruebes o no."

7. **Texto legal** al fondo (11px gris claro):
   Bloque naranja: "⚠️ PENDIENTE LEGAL: aviso legal obligatorio para activación — no publicar sin validación."

**Columna derecha:**
- Ilustración placeholder: rectángulo con gradiente diagonal verde claro `#E8F8ED` → blanco, 100% alto, `border-radius: 12px`
- Ícono familia/escudo verde 64px centrado

**Tono:** Confiable, adulto. El padre siente que tiene el control antes de hacer clic.

---

### Pantalla 12 — Dashboard parental
**Canvas:** Desktop 1280px
**Momento:** Vista principal del padre — resumen del estado financiero de Valentina

Layout: Sidebar izquierda (240px) + área de contenido principal.

**Sidebar (fondo blanco, borde derecho gris claro):**
- Logo Skandia (arriba)
- Navegación vertical:
  - "Inicio"
  - "Mi portafolio"
  - **"Skandia Kids ✦"** — ítem activo (verde, bold, badge verde pequeño)
  - "Configuración"
- Avatar "C" + "Carlos" al fondo del sidebar

**Área de contenido — de arriba hacia abajo:**

**Banner de acción pendiente** (fondo amarillo claro `#FFF9E6`, borde izquierdo naranja 4px, padding 16px):
- Ícono campana naranja izquierda
- Texto: "Valentina quiere sumar $120.000 a 'Mis AirPods'. Tienes una solicitud pendiente."
- Botón secundario derecha (borde, sin relleno): "Ver solicitud"

**Cabecera de sección:**
- Título H2 (Montserrat Bold, 28px): "Así va Valentina"
- Subtítulo (Open Sans 16px, gris): "Aquí ves un resumen de sus metas y movimientos. Entra a su canal para ver todo el detalle."
- Botón primario verde (esquina superior derecha): "Ver canal de Valentina"

**Tarjeta — Meta activa** (fondo blanco, `border-radius: 12px`, sombra suave, borde izquierdo verde 4px):
- Nombre de meta: "Mis AirPods" (bold)
- Barra de progreso verde: 68% relleno
- Texto: "$238.000 de $350.000"
- Chip "En progreso" (verde claro, texto verde)

**Sección — Cursos gratuitos Skandia Channel** (fondo `#003d1a`, padding 32px, `border-radius: 12px`):
- Chip verde claro: "Recursos para ti"
- Título blanco bold 20px: "Herramientas para acompañar a Valentina"
- Subtítulo blanco 14px: "Cursos gratuitos para padres sobre educación financiera infantil."
- Dos tarjetas en fila (fondo blanco con transparencia leve, `border-radius: 8px`, padding 16px):
  - Tarjeta 1: Ícono libro verde · Título "Educación financiera infantil" · Texto gris claro 13px "Skandia Channel" · Botón outlined blanco pequeño "Ver curso →"
  - Tarjeta 2: Ícono familia verde · Título "Niños financieramente conscientes" · Texto gris claro 13px "Skandia Channel" · Botón outlined blanco pequeño "Ver curso →"

**Caja informativa** (si no hay alerta pendiente — fondo `#E8F3FF`, `border-radius: 8px`, padding 16px):
- Ícono info azul
- Texto azul oscuro: "Valentina no ha hecho movimientos esta semana. Todo tranquilo."

---

### Pantalla 06B — Validación PIN · Aporte solicitado por Valentina
**Canvas:** Desktop — modal 480px centrado sobre el dashboard
**Momento:** Valentina solicitó un aporte → el padre recibe notificación y valida con PIN

Modal sobre fondo oscurecido (`rgba(0,0,0,0.4)`). Fondo blanco, `border-radius: 16px`, sombra `0 8px 32px rgba(0,0,0,0.15)`, padding 40px.

**Contenido del modal — de arriba hacia abajo:**

1. **Ícono** campana verde, 48px, centrado

2. **Título** (Montserrat Bold 22px, centrado):
   "Valentina quiere sumar $120.000 a su billetera"

3. **Subtítulo** (Open Sans 16px, gris, centrado):
   "El dinero saldría de tu cuenta Skandia ••••4821."

4. **Campo PIN** (centrado):
   - Label arriba: "Ingresa tu PIN" (14px gris)
   - 6 círculos/inputs enmascarados, espaciados, borde gris → borde verde al enfocar
   - Sin teclado numérico visible en el diseño

5. **Botón primario** verde, ancho completo, altura 48px:
   "Confirmar con PIN"

6. **Botón secundario** outlined (borde gris, texto oscuro), ancho completo:
   "Ver la billetera de Valentina"

7. **Bloque naranja** al fondo (fondo `#FFF3CD`, borde `1px solid #FFA500`, `border-radius: 8px`, padding 12px):
   "⚠️ PENDIENTE LEGAL: aviso legal obligatorio en operaciones — no publicar sin validación."

**Tono:** Claro y directo. El padre sabe exactamente qué está aprobando y de dónde sale el dinero.

---

### Pantalla 07 — Aporte directo del padre
**Canvas:** Desktop 1280px
**Momento:** El padre decide aportar a la billetera de Valentina sin que ella lo haya solicitado

Sidebar igual al dashboard (P12) + área de contenido: formulario centrado, ancho máximo 600px, tarjeta blanca sobre fondo `#F5F5F5`.

**Tarjeta del formulario** (fondo blanco, `border-radius: 12px`, sombra suave, padding 40px):

**Estado formulario (inicial):**

1. **Título** (Montserrat Bold 24px):
   "Suma plata a la billetera de Valentina"

2. **Subtítulo** (Open Sans 16px, gris):
   "El dinero saldrá de tu cuenta vinculada. Valentina verá el cambio en su billetera."

3. **Campo monto** (prominente):
   - Label "Monto a sumar" (14px)
   - Prefijo "$" gris dentro del campo
   - Cifra en IBM Plex Mono Bold 22px
   - Borde gris → borde verde al enfocar

4. **Selector cuenta origen:**
   - Label "Desde tu cuenta" (14px)
   - Dropdown: "Cuenta de ahorro Skandia ••••4821"

5. **Divisor** línea gris claro

6. **Campo PIN:**
   - Label "Confirma con tu PIN" (14px)
   - 6 círculos enmascarados, centrados

7. **Botón primario** verde, ancho completo:
   "Confirmar con PIN"

8. **Bloque naranja** (fondo `#FFF3CD`, borde `1px solid #FFA500`):
   "⚠️ PENDIENTE LEGAL: aviso legal obligatorio — no publicar sin validación."

**Estado éxito** (reemplaza el formulario en el mismo espacio):
- Ícono check verde `fa-circle-check`, 48px, centrado
- Título bold centrado: "Listo. Sumaste $[X] a la billetera de Valentina. Ella ya puede verlo."
- Caja info azul claro (`#E8F3FF`, `border-radius: 8px`, padding 16px): "Valentina ya recibió una notificación con el movimiento."
- Botón secundario outlined centrado: "Volver al portal"

---

### Pantalla 08B — Validación PIN · Retiro solicitado por Valentina
**Canvas:** Desktop — modal 480px centrado sobre el dashboard
**Momento:** Valentina solicitó un retiro → el padre recibe notificación y valida con PIN

Mismo estructura que P06B pero el ícono es naranja para diferenciar visualmente un flujo de salida de dinero.

**Contenido del modal:**

1. **Ícono** flecha saliendo, naranja `#FF8C00`, 48px, centrado

2. **Título** (Montserrat Bold 22px, centrado):
   "Valentina quiere retirar $80.000 de su billetera. Confirma con tu PIN para procesar."

3. **Campo PIN** (centrado):
   - Label: "Ingresa tu PIN"
   - 6 círculos enmascarados

4. **Botón primario** verde, ancho completo:
   "Confirmar con PIN"

5. **Bloque naranja — Operaciones** (fondo `#FFF3CD`, borde `1px solid #FFA500`):
   "⚠️ PENDIENTE OPERACIONES: El retiro se procesa en [X días hábiles] — dato real requerido antes de producción."

6. **Bloque naranja — Legal** (mismo estilo, debajo):
   "⚠️ PENDIENTE LEGAL: aviso legal de retiro — no publicar sin validación."

**Diferenciación visual vs. P06B:**
- Ícono naranja (no verde) para señalar operación de salida de dinero
- El título describe una salida, no una entrada
- Los dos bloques naranjas hacen visible que hay más pendientes en este flujo que en el de aporte

---

## Conexión entre pantallas

```
P01 (Activación)
  └─→ P12 (Dashboard parental) ←─ punto de entrada habitual
        ├─→ P06B (Aprobar aporte solicitado por adolescente)
        ├─→ P07 (Hacer aporte directo)
        └─→ P08B (Aprobar retiro solicitado por adolescente)
```

Los modales P06B y P08B aparecen sobre P12 — el padre no sale de su dashboard para aprobar.

---

*Skandia UX Team · UXplorers Agents · Junio 2026*
