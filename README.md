# Skandia Kids - El Método

> Una plataforma interactiva de educación financiera para padres, diseñada para construir conciencia financiera desde el hogar.

## 🎯 ¿Qué es Skandia Kids?

Skandia Kids es un **método innovador de crianza financiera** que transforma la conversación sobre dinero entre padres e hijos. No es un producto bancario ni una billetera digital: es un **sistema educativo** que ayuda a los padres a entender cómo sus hijos ven las finanzas, y luego les proporciona planes de acción concretos para construir hábitos financieros saludables.

### Flujo Principal

1. **Diagnóstico Interactivo** — El padre responde preguntas sobre su hijo
2. **Generación de Conciencia** — Sistema de reglas genera perfiles y patrones
3. **Planes de Acción** — Recomendaciones personalizadas con métodos probados
4. **Acompañamiento Continuo** — Metas, seguimiento y refuerzo educativo

## 🚀 Características

- ✅ **Diagnóstico adaptativo** — Preguntas que evolucionan según las respuestas
- ✅ **Motor de reglas generativo** — Perfiles personalizados basados en datos
- ✅ **Planes específicos** — Métodos de crianza recomendados (Conversación, Alianza, Billetera, etc.)
- ✅ **Calendario de acciones** — Hoja de ruta mensual con citas clave
- ✅ **Respaldo educativo** — Cursos opcionales para profundizar
- ✅ **Interfaz responsive** — Diseñada para móvil y desktop

## 📁 Estructura del Proyecto

```
skandia_kids/
├── V3_Skandia Kids/
│   ├── Skandia Kids - El Método.dc.html    # Prototipo principal interactivo
│   ├── assets/                              # Logos, SVGs, iconos Skandia
│   ├── support.js                           # Funcionalidades auxiliares
│   └── colors_and_type.css                  # Design system Skandia
├── Sandbox/
│   └── stitch/                              # Documentación de flujos
├── recursos sk kids/
│   ├── Cursos sk channel/                   # Contenido educativo
│   └── investigaciones/                     # Research y hallazgos
└── README.md
```

## 🛠️ Cómo Ejecutar Localmente

### Requisitos
- Un navegador moderno (Chrome, Firefox, Safari, Edge)
- Servidor HTTP local (opcional pero recomendado)

### Opción 1: Con Python (simple)
```bash
cd "V3_Skandia Kids"
python -m http.server 8000
# Abre http://127.0.0.1:8000/Skandia\ Kids\ -\ El\ Método.dc.html
```

### Opción 2: Con Node.js
```bash
npm install -g http-server
cd "V3_Skandia Kids"
http-server
```

### Opción 3: Directamente
Abre `V3_Skandia Kids/Skandia Kids - El Método.dc.html` en tu navegador (funciona, pero algunas features pueden limitarse).

## 🎨 Tecnología

- **Frontend:** HTML5 + CSS3 + Vanilla JavaScript
- **Design System:** Skandia (verde #00c73d, tipografía Montserrat/Open Sans)
- **Datos:** Simulados en cliente (sin backend en MVP)
- **Compatibilidad:** Responsive, mobile-first

## 📋 Flujos Documentados

La carpeta `Sandbox/stitch/` contiene la arquitectura de cada pantalla:
- P01: Portal de entrada
- P02/P03: Diagnóstico interactivo
- P04: Conciencia (resultados personalizados)
- P05: Hub de planes
- P06-P13: Planes detallados, metas, cursos

## 🔄 Estado del Proyecto

**MVP v3** (junio 2026)
- ✅ Diagnóstico funcional
- ✅ Generación de conciencia
- ✅ Planes detallados con abridores de conversación
- ⏳ Integración con billetera Skandia (pendiente Legal/Ops)
- ⏳ Sincronización con app de adolescentes (fase 2)

## 📝 Notas de Desarrollo

- **Datos simulados:** Los datos de metas, aportes y billetera son ejemplos de ejemplo con fines de prototipo
- **Motor generativo:** Actualmente usa reglas explícitas; arquitectura preparada para IA generativa
- **Insignias/Gamificación:** Incluidas a propósito como refuerzo educativo (no es crypto/rewards)

## 🤝 Contribuir

Este es un proyecto de Skandia en desarrollo. Para cambios:
1. Abre un issue describiendo el cambio
2. Crea una rama (`feature/nueva-feature`)
3. Commit con mensajes claros
4. Push y abre un Pull Request

## 📞 Contacto

Proyecto liderado por **Isaac Acosta** — iacostal@skandia.com.co

---

**Skandia Kids es una iniciativa de Skandia Colombia para reinventar la educación financiera familiar.**
