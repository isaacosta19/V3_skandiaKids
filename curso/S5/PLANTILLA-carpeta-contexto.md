# Plantilla — La carpeta `/contexto` 🧠
## El artefacto de la S6 · la memoria de tu proyecto

> Esta es la estructura que le da **memoria persistente** a tu agente. En vez de repetirle tu design system, tus decisiones y tu feature cada vez (y que igual invente), lo dejas **escrito en archivos** que el agente consulta. Es tu **Ficha 4D hecha permanente**: D1 (decisiones) + D2 (specs) + tu design system, viviendo en tu proyecto.

---

## 📁 Estructura
Crea esta carpeta en la raíz de tu proyecto:

```
tu-proyecto/
├── /contexto
│   ├── design.md          ← paleta, tipografía, tokens, principios
│   ├── decisiones.md      ← qué NO delegas, qué cuenta como éxito (tu D1)
│   ├── reglas.md          ← las reglas fijas del agente
│   └── spec-[feature].md  ← una por cada feature (tu D2)
├── ... (tu código/MVP)
```

---

## 1️⃣ `design.md` — tu sistema de diseño
Pega el que ya tienes (S2/S4) o genéralo con el **generador de contexto del curso** (`generadores/prompt-agente-generador-contexto.md`). Mínimo debe incluir:
- Nombre del design system y principios de diseño.
- Paleta con **roles** (primario, superficies, neutrales, semánticos).
- Tipografía y **design tokens** básicos.

---

## 2️⃣ `decisiones.md` — tu criterio (D1)
Corto y claro. Esto evita que el agente decida por ti lo que no debe:
```
# Decisiones del proyecto

QUÉ NO DELEGO (lo decido yo, siempre):
- [ej: cuál es el flujo principal y qué cuenta como éxito]
- [ej: qué datos se le piden al usuario y cuáles no]

QUÉ SÍ DELEGO:
- [ej: maquetación, estados, refactors, datos mock]

QUÉ CUENTA COMO ÉXITO EN ESTE PROYECTO:
- [ej: el flujo X se completa de inicio a fin sin romperse]
```

---

## 3️⃣ `reglas.md` — las reglas del agente
Las restricciones que el agente debe respetar SIEMPRE (tus reglas de orquestador):
```
# Reglas para el agente

- Respeta siempre /contexto/design.md. No inventes colores ni tipografías.
- Usa tokens del design system, nunca valores hardcodeados.
- Reutiliza componentes existentes; no dupliques.
- Pregunta antes de borrar o reescribir archivos que ya funcionan.
- Si cambio el design.md, vuelve a consultarlo antes de generar UI.
- Datos mock, nunca datos reales de usuarios.
- Antes de un cambio grande, propón un plan y espera mi aprobación (modo Plan).
```
> 💡 En algunos agentes este archivo puede llamarse `agent.md` o ir en "rules"/"reglas del proyecto". El contenido es lo que importa.

---

## 4️⃣ `spec-[feature].md` — una por feature (D2)
Usa la **plantilla de spec de la S5** (`charlie-s5-construir-con-un-agente/PLANTILLA-spec-feature.md`). Cada feature que construyas deja su spec aquí. Así el agente recuerda **qué** se construyó y **por qué**.

---

## 🔗 Cómo se la das al agente
Una sola vez por sesión de trabajo, al abrir el proyecto:
```
Lee la carpeta /contexto antes de cualquier cambio.
design.md, decisiones.md y reglas.md son tu fuente de verdad.
Si algo de lo que te pido contradice estos archivos, avísame antes de hacerlo.
```

---

## 🧪 Cómo saber que la memoria funciona
1. Pide un cambio pequeño de UI **sin** repetir la paleta → ¿respeta tu design system solo? ✅
2. Pídele a propósito algo que viole una regla (ej: un color fuera de la paleta) → ¿te avisa? ✅
3. Cambia algo en `design.md` y pide aplicar → ¿lo consulta y lo respeta? ✅

> Si pasa las 3, tu agente ya tiene memoria de tu proyecto.

---

## ⚠️ Recordatorios de criterio (de tu Ficha 4D)
- **El contexto vive en tus archivos**, no en el chat. Lo que no escribes, el agente lo olvida.
- **Mantén `/contexto` actualizado:** cuando cambies una decisión o el design system, edita el archivo — no solo el chat.
- **D4 — diligencia:** datos mock, nunca reales. Y verifica tú; el responsable del resultado sigues siendo tú.

---
_Curso AI para UXers · Wave Charlie · S6 · Plantilla "La carpeta /contexto"._
