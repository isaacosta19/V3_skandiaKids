# Pantalla 11 — Reto desbloqueado
**ID:** reto-unlock
**Canvas:** Mobile 375px — overlay/modal sobre el dashboard
**Actor:** Adolescente
**Posición en el flujo:** Aparece durante el Acto 2 cuando el sistema detecta el momento adecuado

---

## Prompt para Stitch

Diseña un modal o pantalla overlay mobile (375px) que aparece sobre el dashboard de una adolescente de 16 años anunciando que tiene un reto disponible. Debe sentirse como una notificación de juego — que desbloqueas algo — sin ser infantil.

**Layout:** Modal de hoja inferior (bottom sheet) que sube desde abajo. Ocupa aprox. 70% de la pantalla. Esquinas superiores redondeadas. Fondo oscurecido arriba.

**Contenido del modal (de arriba hacia abajo):**
1. Línea de agarre (pill gris centrado) — indica que es un bottom sheet
2. Badge grande con ícono de candado abierto o estrella: "Reto desbloqueado" — fondo verde, texto blanco
3. Título: "Reto desbloqueado" (grande, Montserrat Bold)
4. Descripción del reto en tarjeta con fondo gris claro:
   - Texto: "¿Sabes en qué se va tu plata cada semana? Registra tus 3 gastos más grandes de los últimos 7 días."
5. Recompensa visible: chip con ícono de estrella · "Completa este reto y desbloquea el siguiente nivel"
6. Microcopy en gris muy pequeño: "Este reto es solo tuyo. No se comparte con tu equipo."
7. Botón primario ancho completo: "Empezar reto"
8. Link texto gris centrado: "Más tarde"

**Estilo visual:**
- El badge de "Reto desbloqueado" es el gancho visual principal — debe llamar la atención
- La descripción del reto en tarjeta gris claro lo hace concreto y real
- La recompensa visible (chip) mantiene la motivación antes de aceptar
- El microcopy de privacidad es pequeño pero importante — el adolescente tiene su espacio

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Badge "Reto desbloqueado": fondo `#00C73D`, texto blanco, `border-radius: 20px`, padding `8px 16px`
- Ícono del badge: `fa-lock-open` o estrella blanca
- Bottom sheet: fondo blanco, esquinas superiores `border-radius: 20px`
- Fondo oscurecido: `rgba(0,0,0,0.5)` detrás del sheet
- Pill de agarre: `4px × 32px`, fondo gris `#D0D0D0`, centrado
- Tarjeta descripción reto: fondo `#F5F5F5`, `border-radius: 8px`, padding `12px`
- Chip recompensa: fondo `#E8F8ED`, ícono estrella verde, texto verde oscuro
- Botón primario: verde `#00C73D`, ancho 100%, altura 52px
- Microcopy privacidad: Open Sans 11px, gris claro, centrado
