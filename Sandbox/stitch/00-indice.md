# Índice — Prompts Stitch · Skandia Kids

Usa cada archivo como prompt en Stitch para generar la pantalla correspondiente.
El copy exacto de cada pantalla está en `../skandia-kids-content.md`.
Los tokens de color y tipografía están en `../skandia-design-system.md`.

---

## Orden de construcción recomendado

### Flujo del adolescente (mobile 375px) — primero
| Archivo | Pantalla | Momento del flow |
|---------|----------|-----------------|
| [02-bienvenida-adolescente.md](02-bienvenida-adolescente.md) | Bienvenida | Onboarding paso 1 |
| [03-armar-equipo.md](03-armar-equipo.md) | Armar el equipo | Onboarding paso 2 |
| [04-dashboard-adolescente.md](04-dashboard-adolescente.md) | Dashboard | Pantalla principal |
| [05-crear-meta.md](05-crear-meta.md) | Crear meta | Acción principal |
| [06-solicitar-aporte.md](06-solicitar-aporte.md) — Prompt A | Solicitar aporte | Transacción |
| [08-solicitar-retiro.md](08-solicitar-retiro.md) — Prompt A | Solicitar retiro | Transacción |
| [09-meta-cumplida.md](09-meta-cumplida.md) | Meta cumplida | Momento de logro |
| [10-hacer-crecer.md](10-hacer-crecer.md) | Hacer crecer | Introducción a inversión |
| [11-reto-desbloqueado.md](11-reto-desbloqueado.md) | Reto desbloqueado | Gamificación |
| [13-leccion-1.md](13-leccion-1.md) | Lección 1 — ¿Para qué sirve ahorrar? | Contenido educativo |

### Flujo del padre (desktop 1280px) — segundo
| Archivo | Pantalla | Momento del flow |
|---------|----------|-----------------|
| [01-activacion-parental.md](01-activacion-parental.md) | Activación | Onboarding padre |
| [12-dashboard-parental.md](12-dashboard-parental.md) | Dashboard | Pantalla principal padre |
| [06-solicitar-aporte.md](06-solicitar-aporte.md) — Prompt B | Validación PIN aporte | Modal |
| [07-aporte-directo-padre.md](07-aporte-directo-padre.md) | Aporte directo | Acción del padre |
| [08-solicitar-retiro.md](08-solicitar-retiro.md) — Prompt B | Validación PIN retiro | Modal |

---

## Paleta de marca (referencia rápida)

| Token | Color | Uso |
|-------|-------|-----|
| Verde principal | `#00C73D` | Botones primarios, acentos, progreso |
| Verde claro | `#E8F8ED` | Fondos de badges, chips, éxito |
| Verde texto | `#00703A` | Texto sobre fondos verdes claros |
| Fondo página | `#F5F5F5` | Fondo general (mobile y desktop) |
| Blanco | `#FFFFFF` | Tarjetas, modales |
| Gris borde | `#D0D0D0` | Bordes de campos y tarjetas |
| Naranja alerta | `#FFA500` | Pendientes y alertas de acción |
| Naranja claro | `#FFF3CD` | Fondo de bloques pendientes |

---

## Tipografía

- **Títulos:** Montserrat Bold (700) — 32px H1, 24px H2, 20px H3
- **Cuerpo:** Open Sans Regular/Medium (400/500) — 16px estándar, 14px labels, 12px captions
- **Cifras:** IBM Plex Mono Bold — solo para montos y valores numéricos

---

## Notas importantes

- **Paleta del adolescente:** Energética pero no infantil. Sin emojis masivos, sin paleta pastel de colores primarios.
- **Paleta del padre:** Idéntica al portal Skandia adulto. Sin adaptaciones juveniles.
- **Placeholders naranjas:** Las pantallas 06B, 07, 08B y 10 tienen bloques de advertencia naranja que indican items pendientes de Legal u Operaciones. Deben ser visibles en el diseño.
- **Máximo 2 CTAs por pantalla:** Nunca más de un botón primario verde por pantalla.
