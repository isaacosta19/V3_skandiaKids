# Pantalla 07 — Aporte directo del padre
**ID:** tx-aporte-padre
**Canvas:** Desktop 1280px (sección del portal parental)
**Actor:** Padre — inicia y valida él mismo

---

## Prompt para Stitch

Diseña una pantalla de formulario para desktop (1280px) donde un padre hace un aporte directo al billetera de su hija sin que ella lo haya solicitado. Es parte del portal web para padres de una app financiera.

**Layout:** Contenido centrado, ancho máximo 600px. Fondo gris muy claro, tarjeta blanca con el formulario.

**Contenido de la tarjeta:**
1. Título: "Suma plata al billetera de Valentina"
2. Subtítulo gris: "El dinero saldrá de tu cuenta vinculada. Valentina verá el cambio en su billetera."
3. Campo de monto: label "Monto a sumar" · prefijo "$" · campo numérico grande
4. Selector de cuenta origen: label "Desde tu cuenta" · dropdown con cuenta vinculada (ej: "Cuenta de ahorro Skandia ••••4821")
5. Separador visual (línea gris claro)
6. Campo PIN enmascarado: label "Confirma con tu PIN" · 6 puntos
7. Botón primario: "Confirmar con PIN"
8. Aviso legal en gris claro, 11px: [PENDIENTE LEGAL — mostrar placeholder naranja]

**Después de confirmar (estado de éxito — mostrar en el mismo espacio):**
- Ícono check verde grande centrado
- Texto: "Listo. Sumaste $[X] al billetera de Valentina. Ella ya puede verlo."
- Mensaje info azul claro: "Valentina ya recibió una notificación con el movimiento."
- Botón secundario: "Volver al portal"

**Estilo visual:**
- Tono adulto Skandia — igual que cualquier otra operación del portal web
- Tarjeta blanca sobre fondo gris claro
- El campo de monto es el más prominente visualmente

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Fondo página: `#F5F5F5`
- Tarjeta: fondo blanco, `border-radius: 12px`, sombra suave, padding 32px
- Campo monto: Montserrat Bold 22px para la cifra
- Campo PIN: centrado, 6 inputs enmascarados o círculos
- Botón primario: verde `#00C73D`, texto blanco, altura 48px, ancho 100% de la tarjeta
- Estado éxito: ícono `fa-circle-check` verde 48px centrado
- Mensaje info: fondo `#E8F3FF`, texto azul oscuro, `border-radius: 8px`
