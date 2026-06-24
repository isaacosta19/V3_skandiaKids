# Pantalla 08 — Solicitar retiro
**ID:** tx-retiro-adol (adolescente) + tx-retiro-padre-pin (padre)
**Canvas:** Mobile 375px (adolescente) / Desktop modal (padre)
**Actor:** Dual — adolescente inicia, padre valida con PIN

---

## Prompt A — Vista del adolescente (mobile 375px)

Diseña una pantalla mobile (375px) donde una adolescente de 16 años solicita retirar dinero de su billetera. El flujo NO debe sentirse como "pedir permiso" — es completar un paso del proceso.

**Layout:** Igual que la pantalla de solicitar aporte (06A) pero para retiro.

**Contenido:**
1. Título: "¿Cuánto quieres retirar?"
2. Subtítulo gris: "Tu familia confirma el retiro con su PIN. El dinero llega a [destino definido]."
3. Campo de monto grande: label "Monto a retirar" · prefijo "$" · placeholder "$0"
4. Saldo disponible como referencia debajo del campo: "Disponible: $412.500" en gris pequeño

**CTA fijo al fondo:**
- Botón primario: "Solicitar retiro"

**Toast (al enviar):**
- Info: "Solicitud lista. Cuando tu familia confirme con PIN, el dinero se procesa."

**Nota importante:** Hay un placeholder de pendiente operaciones que debe verse en la pantalla del padre (ver Prompt B).

---

## Prompt B — Vista del padre (modal desktop)

Diseña un modal de confirmación de retiro para desktop. Igual en estructura al modal de aporte (06B) pero para una solicitud de retiro.

**Contenido del modal:**
1. Ícono de retiro (flecha saliendo) en naranja suave — indica una operación de salida de dinero
2. Título: "Valentina quiere retirar $80.000 de su billetera. Confirma con tu PIN para procesar."
3. Campo PIN: 6 puntos enmascarados
4. Botón primario: "Confirmar con PIN"
5. **Bloque de advertencia naranja visible (pendiente operaciones):**
   - Fondo `#FFF3CD`, borde `#FFA500`
   - Texto: "⚠️ PENDIENTE OPERACIONES: El retiro se procesa en [X días hábiles] — dato real requerido antes de producción."
6. Aviso legal al fondo (también placeholder naranja)

**Estilo:** Mismo tono adulto Skandia del modal 06B. El ícono naranja diferencia visualmente este flujo del de aporte.

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Ícono de retiro: naranja `#FF8C00` o similar — diferencia visual del aporte (verde)
- Toast: fondo `#E8F3FF` (info), texto azul oscuro
- Placeholder pendiente: fondo `#FFF3CD`, borde `1px solid #FFA500`, texto `#856404`
- Campo PIN: igual al de la pantalla 06B
- Todo lo demás igual a la pantalla 06
