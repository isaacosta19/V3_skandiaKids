# Pantalla 04 — Dashboard del adolescente
**ID:** home-adol
**Canvas:** Mobile 375px
**Actor:** Adolescente
**Posición en el flujo:** Pantalla principal — hub central de la experiencia del adolescente

---

## Prompt para Stitch

Diseña el dashboard principal de una app financiera mobile (375px) para una adolescente de 16 años llamada Valentina. Esta es la pantalla que ve cada vez que abre la app — debe transmitir control, progreso y energía.

**Layout:** Header fijo + scroll vertical. Secciones bien diferenciadas con espaciado generoso.

**Header (fijo, fondo blanco con sombra sutil):**
- Logo Skandia pequeño a la izquierda
- Chip con texto "Equipo Ramírez" al centro (verde claro, texto verde)
- Ícono de perfil circular a la derecha (inicial "V")

**Sección 1 — Saldo (prominente, primera cosa que se ve):**
- Label pequeño gris: "Tu plata ahora"
- Cifra grande en tipografía monoespaciada: **$412.500**
- Debajo: barra skeleton muy fina en gris claro (simula "actualizando en tiempo real")

**Sección 2 — Tarjeta de meta activa:**
- Tarjeta con borde izquierdo verde grueso (4px)
- Nombre de la meta: "Mis AirPods"
- Barra de progreso verde: 68% completado
- Texto: "$238.000 de $350.000"
- Chip pequeño: "En progreso"

**Sección 3 — Tarjeta de reto desbloqueado (destacada, llamativa):**
- Fondo verde muy claro (no blanco)
- Badge verde: "Reto desbloqueado"
- Texto: "¿Sabes en qué se va tu plata cada semana?"
- Botón secundario pequeño: "Ver reto"

**Sección 4 — Tu zona de aprendizaje (scroll horizontal de tarjetas):**
- Título de sección 14px bold oscuro: "Tu zona de aprendizaje"
- Fila de 3 tarjetas en scroll horizontal (`overflow-x: auto`). Cada tarjeta: 150×180px, `border-radius: 12px`, `padding: 16px`

  **Tarjeta 1 — Nivel 1 (activa, desbloqueada):**
  - Fondo: gradiente diagonal `#003d1a` → `#00c73d`
  - Badge "Nivel 1" blanco pequeño (arriba izquierda)
  - Ícono alcancía blanco 28px centrado
  - Título blanco bold 13px: "¿Para qué sirve ahorrar?"
  - Barra de progreso blanca semitransparente ancho completo: 0% relleno

  **Tarjeta 2 — bloqueada:**
  - Fondo gris `#e8e8e8`, todos los elementos con `opacity: 0.5`
  - Ícono candado gris 28px
  - Título gris 13px: "La magia del interés"
  - Texto 11px gris: "Completa el nivel 1"

  **Tarjeta 3 — bloqueada:**
  - Mismo estilo que tarjeta 2
  - Ícono gráfico de línea gris 28px
  - Título gris 13px: "Gastos que no ves"

**Sección 5 — Acciones rápidas (fila de botones):**
- "Nueva meta" (botón secundario)
- "Sumar plata" (botón secundario)
- "Retirar" (botón secundario)

**Estilo visual:**
- Energético y limpio — no es una app de banco aburrida pero tampoco es infantil
- El saldo es el elemento más importante visualmente: grande, claro, monoespaciado
- Las tarjetas tienen profundidad con sombra sutil
- Verde #00C73D como color dominante de acentos y progreso

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Fondo general: `#F5F5F5` (gris muy claro) para que las tarjetas blancas resalten
- Tarjetas: fondo blanco, `border-radius: 12px`, sombra `0 2px 8px rgba(0,0,0,0.08)`
- Cifra de saldo: IBM Plex Mono o monoespaciada, 36–40px, peso 700, color oscuro
- Barra de progreso: relleno `#00C73D`, fondo `#E8F8ED`
- Botones secundarios: borde gris, fondo blanco, texto oscuro
- Sin emojis ni íconos infantiles
