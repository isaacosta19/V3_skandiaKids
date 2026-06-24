# Prompt MVP — Vista del padre · Skandia Kids
**Para:** Rachel (UX/UI Designer)
**Canal:** Portal web Skandia (desktop) · Sección Kids
**Fecha:** Junio 2026

---

## 1️⃣ Prompt de construcción

```markdown
Actúa como design engineer senior. Construye un MVP funcional y navegable
de la vista del padre en "Skandia Kids", enfocado únicamente en este flujo:

HAPPY PATH del padre:
Ver el dashboard parental (home-padre) →
recibir alerta de solicitud de aporte pendiente →
aprobar el aporte con PIN →
ver confirmación de operación exitosa.

PRODUCTO (qué quiero):

Pantallas del flujo (4, en orden) — todas desktop, dentro del shell
del portal web Skandia actual como sección dedicada:

  P1. home-padre — Dashboard parental
      El padre ve el resumen de su hijo: metas activas con progreso,
      alerta de solicitud pendiente (si existe) y acceso al canal completo.
      Incluir 2 estados:
        — Estado con solicitud pendiente (alerta visible, CTA "Ver solicitud")
        — Estado sin actividad reciente (mensaje de tranquilidad)

  P2. onb-padre — Activación parental (solo para referencia de entrada)
      Una sola pantalla que explica el modelo: hijo crea metas /
      padre aprueba movimientos / ambos ven el progreso.
      CTA principal: "Activar para mi hijo/hija"

  P3. tx-aporte (vista padre) — Validación de solicitud con PIN
      Notificación de solicitud de aporte del hijo.
      Monto, origen del dinero (producto vinculado), campo de PIN enmascarado.
      CTA principal: "Confirmar con PIN" · CTA secundario: "Ver la billetera de [nombre]"
      Aviso legal al final, una línea: ⚠️ Pendiente Legal/Ops

  P4. tx-aporte-padre — Aporte directo del padre (sin solicitud del hijo)
      El padre aporta directamente a la billetera del hijo.
      Monto, cuenta origen, PIN, confirmación.
      Toast post-confirmación: "Listo. Sumaste $[X] a la billetera de [nombre]. El/ella ya puede verlo."

Datos MOCK realistas (1 hijo, consistente en todas las pantallas):
  - Hijo: Valentina Ríos, 15 años
  - Meta activa 1: "Mis Air Force 1" · Objetivo: $180.000 · Progreso: 55% · $99.000 de $180.000
  - Meta activa 2: "Viaje a Medellín" · Objetivo: $300.000 · Progreso: 10% · $30.000 de $300.000
  - Solicitud pendiente: Valentina quiere sumar $50.000 a "Mis Air Force 1"
  - Cuenta origen del padre: Cuenta de Ahorros Skandia ···4821

Estados a incluir:
  — P1 con alerta: solicitud pendiente visible al tope del dashboard
  — P1 sin actividad: "Valentina no ha hecho movimientos esta semana. Todo tranquilo."
  — P3 con campo de PIN vacío (estado inicial) y botón deshabilitado
  — P4 toast de confirmación exitosa

Criterio de éxito: el padre puede ver la solicitud pendiente de Valentina
y aprobarla con PIN en menos de 3 clics desde el dashboard.

PROCESO (cómo quiero que lo abordes):

- Primero proponme un PLAN por fases. No ejecutes hasta que lo apruebe.
- Respeta ESTRICTAMENTE este design system (no inventes colores ni tipografías):
  [👉 PEGA AQUÍ TU skandia-design-system.md COMPLETO]
- Componentes del PRD a usar por pantalla:
    P1: sk-alert · sk-card · sk-progressbar · sk-button (primary + secondary) · sk-badge · sk-tag
    P2: sk-card · sk-button (primary) · sk-tooltip · sk-badge
    P3: sk-dialog o sk-alert · sk-inputmask · sk-button (primary + secondary) · sk-confirmdialog
    P4: sk-inputnumber · sk-select · sk-inputmask · sk-button (primary) · sk-toast · sk-messages
- Microcopy exacto por pantalla (no alterar):

    P1 — home-padre:
      Título sección: "Así va Valentina"
      Subtítulo: "Aquí ves un resumen de sus metas y movimientos. Entra a su canal para ver todo el detalle."
      Estado de meta: "[Nombre de meta]: [%] completada · $[monto] de $[total]"
      CTA acceso canal: "Ver canal de Valentina"
      Alerta pendiente: "Valentina quiere sumar $50.000 a 'Mis Air Force 1'. Tienes una solicitud pendiente."
      CTA validación: "Ver solicitud"
      Sin actividad: "Valentina no ha hecho movimientos esta semana. Todo tranquilo."

    P2 — onb-padre:
      Título: "Tu hijo aprende a manejar su plata. Tú siempre sabes cómo va."
      Subtítulo: "Skandia Kids es un espacio donde tu hijo practica con dinero real,
                  con metas que él elige y movimientos que tú apruebas."
      CTA principal: "Activar para mi hijo/hija"
      Microcopy bajo CTA: "Tú controlas cada movimiento. Tu hijo tiene la experiencia."
      Tooltip: "Cada vez que tu hijo quiera mover plata, te llegará una notificación
                para que tú apruebes o no."

    P3 — tx-aporte (vista padre):
      Título notificación: "Valentina quiere sumar $50.000 a su billetera"
      Subtítulo: "El dinero saldría de tu cuenta de Ahorros Skandia ···4821."
      CTA principal: "Confirmar con PIN"
      CTA secundario: "Ver la billetera de Valentina"
      Aviso legal: ⚠️ "Operación realizada bajo normativa vigente para productos de menores de edad."
                   [Marcar visualmente como PENDIENTE LEGAL/OPS]

    P4 — tx-aporte-padre:
      Título: "Suma plata a la billetera de Valentina"
      Subtítulo: "El dinero saldrá de tu cuenta vinculada. Valentina verá el cambio en su billetera."
      CTA: "Confirmar con PIN"
      Toast: "Listo. Sumaste $50.000 a la billetera de Valentina. Ella ya puede verlo."

- El tono visual de las pantallas del padre es Skandia adulto estándar —
  no infantilizar, no colores ni energía del flujo del adolescente.
  Es una sección especializada dentro del portal, no una app separada.
- Los elementos 🔴 bloqueantes (avisos legales, plazo de retiro) deben
  marcarse visualmente como "⚠️ Pendiente Legal/Ops". No los omitas.
- Reutiliza componentes. No dupliques. No inventes datos ni endpoints.

DESEMPEÑO (cómo quiero que trabajes):

- Entregable: archivo .html autocontenido, desktop (viewport mínimo 1280px).
  Simula el shell del portal Skandia actual — la sección Kids vive dentro,
  no es un portal independiente.
- Sé conciso. Si algo es ambiguo, pregúntame antes de asumir.
- No agregues pantallas que no estén en este flujo: sin flujo de retiro,
  sin dashboard del adolescente, sin módulo "hacer crecer", sin login.

Empieza mostrándome solo el PLAN.
```

---

## 2️⃣ Prompt de evaluación

```
Antes de avanzar, evalúa lo que generaste con honestidad:

- Producto:
  ¿El padre puede ver la solicitud pendiente de Valentina desde el dashboard?
  ¿Puede aprobarla con PIN en P3 en menos de 3 clics?
  ¿P1 muestra los 2 estados (con solicitud / sin actividad)?
  ¿El aviso legal de P3 está marcado como "⚠️ Pendiente Legal/Ops"?
  ¿El toast de P4 aparece después de confirmar?

- Proceso:
  ¿Seguiste el plan acordado?
  ¿Usaste los componentes sk-* especificados por pantalla?
  ¿El microcopy corresponde exactamente al listado del prompt?

- Desempeño:
  ¿El tono visual es Skandia adulto (no infantilizado)?
  ¿Agregaste pantallas o features que no te pedí?
  ¿Cambiaste la paleta o la tipografía?

Dime qué falló y propón la corrección mínima.
```

---

## 3️⃣ Prompts de refinamiento

```
Agrega el estado "sin actividad reciente" en P1: el mensaje de tranquilidad
visible cuando Valentina no ha tenido movimientos esta semana. No toques nada más.
```

```
El aviso legal de P3 no está marcado como pendiente. Agrégale el indicador
visual "⚠️ Pendiente Legal/Ops" sin cambiar el layout.
```

```
El flujo se rompe cuando [describe el problema]. Arréglalo sin cambiar el diseño ni la paleta.
```

```
El microcopy de [pantalla] no corresponde al listado del prompt.
Reemplaza solo ese texto. No toques el diseño.
```

---

## 4️⃣ Cerrar y exportar

```
Genera la versión final estable del MVP del flujo del padre lista para exportar.
Confírmame que: el padre ve la solicitud de Valentina en P1 → entra a P3 →
confirma con PIN → ve el toast de confirmación. Los 2 estados de P1 funcionan.
```

---

## ⚠️ Restricciones no negociables

- Los avisos legales de P3 y P4 son **🔴 bloqueantes** — no van a producción
  sin validación de Legal. En el prototipo van marcados, no omitidos.
- El PIN puede ser placeholder en el MVP, pero el campo debe existir
  y el botón debe estar deshabilitado hasta que se ingrese algo.
- El tono visual es **Skandia adulto** en todas las pantallas del padre.
  Ninguna pantalla de este flujo debe parecer diseñada para niños.
- Nada promete rendimientos ni resultados financieros.
```
