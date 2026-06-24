# Mega-prompt reutilizable — Prompt to MVP 🛠️
## El artefacto de la S4 · cópialo, rellénalo y reúsalo

> Este es el prompt con el que conviertes tu UI en un MVP funcional. Está estructurado con las **3 capas de tu D2** (Producto · Proceso · Desempeño), así que tu Ficha 4D ya hizo medio trabajo. Rellena lo que está entre `[corchetes]` y **pega tu `design.md` completo** donde se indica.

---

## 1️⃣ Prompt principal — genera el MVP
Cópialo en **AI Studio** (o tu herramienta), rellénalo y envíalo:

```
Actúa como design engineer senior. Construye un MVP funcional y navegable de "[NOMBRE DEL PROYECTO]", enfocado únicamente en este flujo: [HAPPY PATH, ej: registrar X → verlo reflejado en Y].

PRODUCTO (qué quiero):
- Pantallas del flujo: [lista las pantallas mínimas, ej: 1) formulario, 2) dashboard].
- Datos: usa datos MOCK realistas (3-5 ejemplos). Sin backend, sin base de datos real.
- Estados: incluye estado vacío y estado con datos.
- Criterio de éxito: puedo completar el flujo de inicio a fin sin que se rompa.

PROCESO (cómo quiero que lo abordes):
- Primero proponme un PLAN por fases. No ejecutes hasta que lo apruebe.
- Respeta ESTRICTAMENTE este design system (no inventes colores ni tipografías):
[👉 PEGA AQUÍ TU design.md COMPLETO]
- Reutiliza componentes; no dupliques. No inventes endpoints ni datos que no pedí.

DESEMPEÑO (cómo quiero que trabajes):
- Sé conciso. Si algo es ambiguo, pregúntame antes de asumir.
- No agregues features que no estén en el flujo (sin login, sin ajustes, sin extras).

Empieza mostrándome solo el PLAN.
```

---

## 2️⃣ Prompt de evaluación — tu D3 (Discernimiento)
Después de generar, **evalúa antes de seguir pidiendo cosas**:

```
Antes de avanzar, evalúa lo que generaste con honestidad:
- Producto: ¿el flujo se completa de inicio a fin? ¿respeta los tokens y la jerarquía del design system? ¿el CTA principal es lo más prominente?
- Proceso: ¿seguiste el plan que acordamos o improvisaste? ¿reutilizaste componentes?
- Desempeño: ¿agregaste pantallas, datos o features que NO te pedí? ¿cambiaste la paleta?
Dime qué falló y propón la corrección mínima.
```

---

## 3️⃣ Prompts de refinamiento — pequeños y dirigidos
Un cambio a la vez. Así no rompes lo que ya funciona:

```
Agrega el estado vacío de [pantalla] con un mensaje amable y el CTA correcto. No toques nada más.
```
```
El flujo se rompe cuando [describe el problema]. Arréglalo sin cambiar el diseño ni la paleta.
```
```
Haz que [elemento] respete el token [nombre del token] de mi design system. Solo ese cambio.
```

---

## 4️⃣ Antes de cerrar — exportar
```
Genera la versión final estable de este MVP lista para exportar. Confírmame que el flujo completo funciona con los datos mock.
```
Luego: **Export** en AI Studio → descomprime → guarda junto a tu `design.md` y tu Ficha 4D.

---

## ⚠️ Recordatorios de criterio (de tu Ficha 4D)
- **D1 — qué NO delegas:** la decisión de cuál es el flujo principal y qué cuenta como éxito es **tuya**, no de la IA.
- **D4 — diligencia:** **datos mock, nunca datos reales de usuarios** en el MVP. Y el responsable del resultado eres tú: verifica antes de mostrarlo.
- **Alcance:** si te sientes tentado a pedir "una pantalla más", anótala para la S5. Hoy: **un flujo**.

---
_Curso AI para UXers · Wave Charlie · S4 · Mega-prompt reutilizable "Prompt to MVP"._
