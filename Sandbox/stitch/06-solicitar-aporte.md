# Pantalla 06 — Solicitar aporte
**ID:** tx-aporte-adol (vista adolescente) + tx-aporte-padre-pin (vista padre)
**Canvas:** Mobile 375px (adolescente) / Desktop modal (padre)
**Actor:** Dual — adolescente inicia, padre valida con PIN

---

## Prompt A — Vista del adolescente (mobile 375px)

Diseña una pantalla mobile (375px) donde una adolescente de 16 años solicita que se traslade dinero a su billetera. Debe sentirse ágil — no un trámite.

**Layout:** Pantalla simple en columna. Header con flecha atrás. CTA fijo al fondo.

**Contenido:**
1. Título: "¿Cuánto quieres sumar a tu billetera?"
2. Subtítulo gris: "Tu familia recibirá una notificación para confirmar el traslado."
3. Campo de monto grande y prominente: label "Monto a sumar" · placeholder "$0" · la cifra del campo debe ser grande (24px) para enfatizar el monto
4. Selector opcional en gris claro: "Asociar a una meta (opcional)" — dropdown con "Mis AirPods" como opción

**CTA fijo al fondo:**
- Botón primario: "Solicitar aporte"

**Toast (mostrar al enviar):**
- Verde claro, ícono check: "Solicitud enviada. Cuando tu familia lo confirme con su PIN, el dinero llega a tu billetera."

**Estilo:** Limpio, directo. El campo de monto es el protagonista visual — grande y centrado.

---

## Prompt B — Vista del padre (modal desktop)

Diseña un modal de confirmación para desktop donde un padre valida la solicitud de aporte de su hija con un PIN. El modal debe transmitir control y claridad.

**Tamaño del modal:** 480px de ancho, centrado en pantalla. Fondo oscurecido detrás.

**Contenido del modal:**
1. Ícono de notificación en verde (campana o similar) centrado
2. Título: "Valentina quiere sumar $120.000 a su billetera"
3. Subtítulo gris: "El dinero saldría de tu cuenta [Cuenta vinculada Skandia]."
4. Campo PIN enmascarado: 6 puntos o asteriscos — label: "Ingresa tu PIN"
5. Botón primario: "Confirmar con PIN"
6. Botón secundario (link o outlined): "Ver detalles del billetera"
7. Texto legal en gris muy claro, 11px, al fondo del modal: [aviso legal pendiente — placeholder en naranja claro indicando "PENDIENTE LEGAL"]

**Estilo:** Tono adulto Skandia. Sin elementos de la experiencia del adolescente. Serio y claro.

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Campo monto: borde `2px solid #00C73D` (ya enfocado), cifra `24px Montserrat Bold`
- Campo PIN: 6 círculos o inputs cuadrados enmascarados, alineados al centro
- Botón primario modal: verde `#00C73D`, texto blanco, altura 48px
- Modal: fondo blanco, `border-radius: 16px`, sombra `0 8px 32px rgba(0,0,0,0.15)`
- Toast: fondo `#E8F8ED`, texto verde oscuro, ícono `fa-circle-check`
- Placeholder legal pendiente: fondo `#FFF3CD`, borde `1px solid #FFA500`, texto naranja
