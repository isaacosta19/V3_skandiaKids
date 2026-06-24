# Pantalla 12 — Dashboard parental
**ID:** home-padre
**Canvas:** Desktop 1280px
**Actor:** Padre / cuidador
**Posición en el flujo:** Pantalla principal del portal web del padre — acceso al canal de su hijo/a

---

## Prompt para Stitch

Diseña la pantalla principal del portal web para padres (desktop 1280px) de una app financiera llamada Skandia Kids. El padre ve el resumen del progreso de su hija Valentina y puede acceder al canal completo cuando quiera.

**Layout:** Sidebar de navegación izquierda (ancho 240px) + área de contenido principal. El contenido sigue el estilo del portal Skandia adulto — no tiene elementos de la app del adolescente.

**Sidebar (navigation — Skandia adulto estándar):**
- Logo Skandia
- Links de navegación: "Inicio", "Mi portafolio", "Skandia Kids ✦" (sección activa resaltada), "Configuración"
- Avatar del usuario + nombre "Carlos" al fondo

**Área de contenido principal:**

*Sección 1 — Alerta de acción pendiente (si hay solicitud activa — mostrar primero):*
- Banner de alerta amarillo suave (fondo `#FFF3CD`, borde `#FFA500` izquierdo 4px)
- Ícono de campana naranja
- Texto: "Valentina quiere sumar $120.000 a 'Mis AirPods'. Tienes una solicitud pendiente."
- Botón secundario pequeño: "Ver solicitud"

*Sección 2 — Cabecera de sección:*
- Título H2: "Así va Valentina"
- Subtítulo gris: "Aquí ves un resumen de sus metas y movimientos. Entra a su canal para ver todo el detalle."
- Botón primario a la derecha: "Ver canal de Valentina"

*Sección 3 — Tarjeta de meta activa:*
- Tarjeta blanca con sombra suave
- Nombre: "Mis AirPods"
- Barra de progreso verde: 68%
- Texto: "$238.000 de $350.000"
- Tag "En progreso" en verde claro

*Sección 4 — Mensaje de tranquilidad (si no hay más actividad):*
- Caja info azul muy claro: ícono `ℹ️` · "Valentina no ha hecho movimientos esta semana. Todo tranquilo."

**Estilo visual:**
- Idéntico al portal Skandia adulto — mismo nivel de profesionalismo
- Sin ningún elemento de la experiencia del adolescente (sin badges de retos, sin energía juvenil)
- La sección "Skandia Kids" es una extensión natural del portal del adulto
- El botón "Ver canal de Valentina" es el CTA principal de toda la pantalla

---

## Restricciones de marca Skandia
- Verde: `#00C73D`
- Sidebar: fondo `#1A1A2E` o gris oscuro (seguir el estilo del portal Skandia)
- Fondo área contenido: `#F5F5F5`
- Tarjeta meta: fondo blanco, `border-radius: 12px`, sombra `0 2px 8px rgba(0,0,0,0.08)`
- Alerta pendiente: fondo `#FFF3CD`, borde izquierdo `4px solid #FFA500`
- Barra de progreso: relleno `#00C73D`, fondo `#E8F8ED`
- Tag "En progreso": fondo `#E8F8ED`, texto `#00703A`
- Mensaje tranquilidad: fondo `#E8F3FF`, texto azul oscuro
- Botón primario: verde `#00C73D`, texto blanco, altura 40px (desktop — más compacto que mobile)
