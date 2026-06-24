# PRD — Skandia Kids
**Fecha:** 8 de junio de 2026
**Estratega:** Harvey · UX Estratega · Skandia UX Team
**Para:** Rachel (ux-ui-designer)
**Insumos:** skandia-kids-research.md ✅ · skandia-kids-content.md ✅

---

## 1. Contexto

- **Caso:** Experimento de educacion financiera supervisada para adolescentes 13–17 anos con supervision parental obligatoria
- **Canal:** El experimento se construye **dentro de los activos actuales de Skandia** — no es una app ni un portal independiente. El adolescente accede desde una sección dedicada dentro de la **app Skandia existente**. El padre accede desde una sección dedicada dentro del **portal web Skandia existente**. Ambos usan sus credenciales actuales.
- **Segmento principal — adolescente:** Financial Explorer en formacion. 13–17 anos. Primer contacto real con un producto financiero propio. Aprende por accion, no por contenido teorico. Alta intolerancia a la friccion y al tono condescendiente.
- **Segmento secundario — padre/cuidador:** Family Guardian. Alta motivacion para desarrollar habitos financieros en su hijo. Detonante emocional: la universidad. Necesita control visible y sin micromanagement. Muy motivado pero con ansiedad latente sobre autonomia del menor.
- **Outcome de negocio:** Disenar y validar un experimento que demuestre que los adolescentes de 13–17 anos pueden desarrollar agencia financiera real dentro de un entorno supervisado de Skandia — abriendo un segmento nuevo para la compania.
- **Problema del usuario (adolescente):** No tiene agencia directa sobre su propio dinero. Depende del adulto para saber cuanto tiene, para moverlo y para entenderlo. No existe una experiencia financiera disenada para el como usuario directo.
- **Problema del usuario (padre):** Quiere ensearle a su hijo a manejar dinero pero no tiene la herramienta ni el metodo. El detonante es la universidad: el momento de ensearle ya paso o esta pasando.
- **Como medir el exito:**
  - Interes espontaneo del adolescente en aprender y practicar sin necesidad de que el padre lo empuje
  - Seguimiento activo del padre en la evolucion financiera del hijo — se involucra porque quiere, no porque toca
- **Promesa central de contenido:** "Tu plata, tu camino — con un equipo que te respalda." *(Para padres: "Tu hijo tiene su propio espacio financiero. Tu eres parte de su equipo.")*

---

## 2. Clasificacion de riesgo

| Dimension | Nivel | Razon |
|---|---|---|
| Regulatorio | ROJO Alto | Contrato financiero para menor de edad. Transacciones reales con validacion parental por PIN. Introduccion a productos de inversion ("hacer crecer"). Multiples obligaciones de disclosure pendientes de validacion legal. Copy de riesgo del Momento 6 depende del producto subyacente. |
| Usabilidad | ROJO Alto | Dos usuarios con modelos mentales opuestos: adolescente (primer contacto con finanzas, alta intolerancia a friccion) y padre (ansiedad de control). Flujo de mas de 5 pantallas con bifurcacion de actor. Primera interaccion del adolescente con un producto financiero propio. Riesgo de abandono documentado desde Joven Go por exceso de texto y clicks. |
| Tecnico | ROJO Alto | Saldo en tiempo real. Validacion por PIN parental. Notificaciones push bidireccionales (adolescente-padre). Contrato activo en el core de Skandia. Dos canales simultaneos (app y portal). Vistas diferenciadas por actor para la misma transaccion. Posible integracion con productos de inversion en Momento 6. |
| Negocio | ROJO Alto | Experimento de adquisicion de segmento nuevo para Skandia. Un error en la experiencia destruye la confianza de todo el nucleo familiar en la marca. El detonante emocional del padre (universidad) es de alto valor percibido. Riesgo reputacional significativo si la experiencia falla. |

**Nivel compuesto: ROJO — Riesgo Alto (4 de 4 dimensiones en rojo)**

**Implicacion:** Sprint de research adicional obligatorio antes de produccion — especificamente para explorar la tension autonomia vs. control parental (pendiente documentado en research.md). El diseno puede avanzar en paralelo pero no va a produccion sin esos hallazgos y sin validacion legal de los puntos 🟡 documentados en la seccion 6.

---

## 3. Estructura del flujo

**Tipo:** C — Narrativa con bifurcacion de actor

Este no es un flujo lineal unico. Tiene dos protagonistas con arcos emocionales distintos que convergen en los momentos de validacion transaccional. La estructura narrativa opera en dos carriles paralelos.

### Flujo A — Adolescente (3 actos)

**Acto 1 · Activacion:** "Este espacio es mio."
El adolescente entra, rompe el escepticismo inicial ("esto es una app de banco para ninos") y entiende que tiene agencia real. Construye su equipo, ve su saldo, crea su primera meta. El objetivo emocional de este acto: propiedad y pertenencia.

**Acto 2 · Practica:** "Aprendo haciendo."
El adolescente vive el ciclo de meta → aporte → progreso → logro. Completa microretos. El vocabulario financiero aparece como algo natural, no como imposicion. El padre existe como parte del equipo, no como obstaculo. El objetivo emocional: competencia y progreso concreto.

**Acto 3 · Crecimiento:** "Mi plata puede hacer mas."
El adolescente tiene su primera exposicion al concepto de hacer crecer (inversion). Entiende la diferencia entre guardar y hacer crecer. Tiene la opcion de explorar sin presion. El objetivo emocional: curiosidad y ambicion positiva.

### Flujo B — Padre/cuidador (2 actos)

**Acto 1 · Habilitacion:** "Entiendo como funciona y lo activo con confianza."
El padre entiende el modelo de supervision (nada se mueve sin su PIN), activa la cuenta del hijo y siente que tiene control real. El objetivo emocional: seguridad y confianza.

**Acto 2 · Seguimiento activo:** "Estoy presente sin tener que intervenir todo el tiempo."
El padre ve el progreso de su hijo en su portal, recibe notificaciones cuando importa, aprueba o rechaza solicitudes. La app hace la conversacion sobre dinero en casa mas natural. El objetivo emocional: involucramiento tranquilo, no ansiedad de control.

### Puntos de intersection entre flujos

Los dos arcos narrativos convergen en los momentos transaccionales:
- **Momento 4A** — El adolescente solicita aporte. El padre valida con PIN.
- **Momento 4B** — El padre aporta directamente a la billetera del hijo.
- **Momento 4C** — El adolescente solicita retiro. El padre valida con PIN.
- **Momento 5** — El padre recibe notificacion cuando el hijo cumple una meta.

En estos momentos, la experiencia debe ser coherente para ambos actores — el mismo evento se narra desde dos perspectivas distintas con el mismo tono de equipo, nunca como vigilancia.

---

## 4. Arquitectura de informacion

---

### Pantalla 01 — Activacion parental (onb-padre)

- **Actor:** Padre/cuidador
- **Acto:** Acto 1 del Flujo B
- **Job:** El padre entiende que es Skandia Kids, como funciona la supervision y activa el espacio para su hijo con confianza.
- **Jerarquia de contenido:**
  1. Titulo principal — la promesa del producto desde la perspectiva del padre
  2. Modelo de operacion en 3 puntos visuales: el hijo crea metas / el padre aprueba movimientos / ambos ven el progreso
  3. CTA de activacion principal
  4. Microcopy de seguridad que refuerza el control
  5. Tooltip explicativo sobre como funciona la aprobacion por PIN
  6. Aviso legal minimo (una linea, al final)
- **Componentes sk-*:**
  - `sk-card` → contenedor del modelo de 3 puntos visuales
  - `sk-button` (primary) → "Activar para mi hijo/hija"
  - `sk-tooltip` → explicacion del mecanismo de aprobacion
  - `sk-badge` → indicadores visuales de los 3 pilares del modelo
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Tu hijo aprende a manejar su plata. Tu siempre sabes como va."
  - Subtitulo: "Skandia Kids es un espacio donde tu hijo practica con dinero real, con metas que el elige y movimientos que tu apruebas."
  - CTA principal: "Activar para mi hijo/hija"
  - Microcopy bajo CTA: "Tu controlas cada movimiento. Tu hijo tiene la experiencia."
  - Tooltip: "Cada vez que tu hijo quiera mover plata, te llegara una notificacion para que tu apruebes o no."
- **Restricciones:**
  - 🟡 El aviso legal de esta pantalla debe ser validado con Legal — confirmar que el texto de una linea cumple los requisitos de disclosure para activacion de producto de menor de edad.
- **Qué activa el CTA "Activar para mi hijo/hija":** Habilita la **billetera Kids** dentro del producto existente del padre en Skandia — no abre un producto a nombre del menor. El padre asocia a su hijo (nombre, datos básicos) y queda como responsable del PIN de validación. Sin contrato nuevo ni documentación del menor para la fase de experimento.
- **Transicion:** Viene del portal Skandia del adulto (seccion Kids o acceso directo). Va hacia la captura de datos del hijo (nombre, edad) y luego al dashboard parental (P12).

---

### Pantalla 02 — Bienvenida del adolescente (onb-adol-01)

- **Actor:** Adolescente
- **Acto:** Acto 1 del Flujo A
- **Job:** Romper el escepticismo inicial. El adolescente entiende que este espacio es suyo — no el de sus papas, no una simulacion — y quiere explorar.
- **Jerarquia de contenido:**
  1. Titulo de agencia directa — lo primero que ve es que esto es suyo
  2. Subtitulo que presenta las tres capacidades concretas (metas, ver como crece, aprender practicando)
  3. CTA principal orientado a accion inmediata
  4. Microcopy que presenta la supervision como equipo, no como limite
- **Componentes sk-*:**
  - `sk-button` (primary) → "Crear mi primera meta"
  - `sk-button` (tertiary) → "Explorar primero" (alternativa sin presion)
  - `sk-card` → contenedor de presentacion con ilustracion o visual de identidad del producto
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Esta es tu plata. Aqui decides que hacer con ella."
  - Subtitulo: "Puedes crear metas, ver como crece tu dinero y aprender como funcionan las inversiones — practicando de verdad."
  - CTA principal: "Crear mi primera meta"
  - Microcopy de supervision: "Para mover plata, tu equipo da el visto bueno. Tu pones la direccion."
  - Mensaje secundario: "Para que quieres guardar tu plata? Eso lo decides tu."
- **Restricciones:**
  - 🟡 La palabra "inversiones" en el subtitulo debe revisarse con Legal — confirmar si su uso en esta pantalla activa obligaciones de disclosure adicionales para menores.
- **Transicion:** Viene del flujo de activacion parental (el padre activo la cuenta). El adolescente ingresa por primera vez. Va hacia la pantalla de armado del equipo (onb-adol-02).

---

### Pantalla 03 — Armar el equipo (onb-adol-02)

- **Actor:** Adolescente
- **Acto:** Acto 1 del Flujo A
- **Job:** El adolescente nombra a los miembros de su equipo (padre/familiar ya vinculado) y puede darle nombre propio al equipo. Skandia se presenta como coach financiero del equipo.
- **Jerarquia de contenido:**
  1. Titulo que activa el frame de equipo — no de supervision
  2. Lista de miembros ya vinculados (padre/familiar aparece automaticamente desde la activacion parental)
  3. Campo opcional para el nombre del equipo
  4. Presentacion de Skandia como coach — breve, sin protagonismo
  5. CTA para continuar
- **Componentes sk-*:**
  - `sk-input` → campo para nombre del equipo (placeholder: "Equipo Garcia", "Los Romero", nombre libre)
  - `sk-card` → tarjeta de cada miembro del equipo con nombre y rol
  - `sk-badge` → etiqueta de rol ("Tu equipo" / "Coach Skandia")
  - `sk-button` (primary) → "Empezar con mi equipo"
  - `sk-chip` → indicador del rol de Skandia como coach
- **Microcopy clave** *(derivado de la mecanica de equipo del content.md)*:
  - Titulo: "Tu equipo ya esta listo."
  - Subtitulo: "Aqui estan las personas que te acompanan. Cuando haya movimientos de plata, ellos dan el visto bueno."
  - Label campo de nombre: "Dale un nombre a tu equipo (opcional)"
  - Placeholder: "Equipo Garcia, Los Romero, el nombre que quieras..."
  - Descripcion coach Skandia: "Skandia es el coach financiero de tu equipo. Aparece cuando hay algo nuevo que aprender o cuando puedes hacer mas con tu plata."
  - CTA: "Empezar con mi equipo"
- **Restricciones:**
  - 🟡 Confirmar con Legal si el nombre "Skandia coach" o "coach financiero" requiere alguna aclaracion de alcance bajo normativa de asesoria financiera.
- **Transicion:** Viene de onb-adol-01. Va hacia home-adol (dashboard del adolescente). Si el adolescente eligio "Crear mi primera meta" en la pantalla anterior, puede ir directamente a meta-crear.

---

### Pantalla 04 — Dashboard del adolescente (home-adol)

- **Actor:** Adolescente
- **Acto:** Transversal — es la pantalla central del Flujo A
- **Job:** Ver en un vistazo cuanto tengo, como van mis metas y que retos tengo disponibles. Es el hub desde donde el adolescente navega toda su experiencia.
- **Jerarquia de contenido:**
  1. Saldo total en tiempo real — dato mas importante, visual y prominente
  2. Metas activas con progreso visual (nombre, porcentaje, monto vs. total)
  3. Microreto disponible — si hay uno desbloqueado, aparece como tarjeta destacada
  4. Acceso a crear nueva meta
  5. Acceso a solicitar aporte o retiro
  6. Logros recientes (si aplica — seccion secundaria)
- **Componentes sk-*:**
  - `sk-card` → tarjeta de cada meta activa
  - `sk-progressbar` → barra de progreso por meta (% completado)
  - `sk-metergroup` → si se necesita comparar multiples metas en un solo visual
  - `sk-badge` → indicador de reto disponible / logro desbloqueado
  - `sk-button` (primary) → "Nueva meta"
  - `sk-button` (secondary) → "Sumar plata" / "Retirar"
  - `sk-skeleton` → estado de carga mientras el saldo en tiempo real se actualiza
  - `sk-chip` → etiqueta de estado por meta ("En progreso", "Lista para retirar")
- **Microcopy clave** *(derivado del content.md)*:
  - Titulo de seccion saldo: "Tu plata ahora"
  - Titulo de seccion metas: "Tus metas"
  - Estado de meta: "[Nombre de meta]: [%] completada · $[monto] de $[total]"
  - Tarjeta de reto: "Reto desbloqueado — [nombre del reto]" + CTA "Ver reto"
  - Estado vacio (sin metas): "Todavia no tienes metas. Crear una toma menos de un minuto."
  - CTA estado vacio: "Crear mi primera meta"
- **Restricciones:**
  - 🟡 El saldo en tiempo real requiere integracion con el core de Skandia. Confirmar con Tecnologia el endpoint disponible y el tiempo de actualizacion.
- **Transicion:** Es la pantalla principal — se llega desde onb-adol-02 y desde cualquier navegacion interna. Desde aqui se puede ir a meta-crear, tx-aporte, tx-retiro, crecer-intro, reto-unlock.

---

### Pantalla 05 — Crear meta (meta-crear)

- **Actor:** Adolescente
- **Acto:** Acto 1 → 2 del Flujo A (es el primer momento de accion real)
- **Job:** El adolescente define su primera meta. El proceso es rapido, personal y suyo — sin opciones predefinidas impuestas.
- **Jerarquia de contenido:**
  1. Titulo-pregunta que invita a la reflexion
  2. Campo de nombre de la meta (libre, con ejemplos cercanos)
  3. Campo de monto objetivo
  4. Campo de fecha (con opcion "sin fecha por ahora")
  5. Opcion de imagen o emoji representativo (si aplica — capa de personalizacion)
  6. CTA de creacion
  7. Microcopy de confirmacion — avisa que el equipo puede ver la meta
- **Componentes sk-*:**
  - `sk-input` → campo de nombre de la meta
  - `sk-inputnumber` → campo de monto objetivo
  - `sk-select` o `sk-input` tipo date → fecha objetivo
  - `sk-checkbox` → opcion "sin fecha por ahora"
  - `sk-button` (primary) → "Crear esta meta"
  - `sk-button` (tertiary) → "Cancelar" / volver
  - `sk-toast` → confirmacion de meta creada
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Para que quieres guardar?"
  - Placeholder nombre de meta: "Ej: mis tenis, viaje a Santa Marta, mi primer millon"
  - Label monto: "Cuanto necesitas?"
  - Label fecha: "Para cuando?"
  - Opcion sin fecha: "Sin fecha por ahora"
  - CTA: "Crear esta meta"
  - Toast confirmacion: "Meta creada. Tu equipo ya la puede ver."
- **Restricciones:**
  - 🟡 Los ejemplos del placeholder deben validarse con adolescentes reales del segmento del experimento antes de produccion.
- **Transicion:** Viene de home-adol o de onb-adol-01 (si el adolescente eligio crear meta de entrada). Va hacia home-adol con la nueva meta visible.

---

### Pantalla 06 — Solicitar aporte (tx-aporte)

- **Actor dual:** Adolescente (inicia) / Padre (valida con PIN)
- **Acto:** Acto 2 del Flujo A · Acto 2 del Flujo B
- **Job del adolescente:** Solicitar que se traslade dinero a su billetera. El flujo es agil — no es un tramite.
- **Job del padre:** Recibir la solicitud y validar o rechazar con PIN.

**Vista del adolescente:**

- **Jerarquia de contenido:**
  1. Titulo de accion directa
  2. Campo de monto
  3. Selector de meta de destino (opcional — el aporte puede ser al saldo general)
  4. Subtitulo que presenta la validacion como paso natural
  5. CTA de solicitud
  6. Confirmacion de solicitud enviada con explicacion del siguiente paso
- **Componentes sk-*:**
  - `sk-inputnumber` → campo de monto
  - `sk-select` → selector de meta de destino (opcional)
  - `sk-button` (primary) → "Solicitar aporte"
  - `sk-toast` → confirmacion de solicitud enviada
  - `sk-messages` → mensaje de estado mientras el padre valida
- **Microcopy clave adolescente** *(de skandia-kids-content.md)*:
  - Titulo: "Cuanto quieres sumar a tu billetera?"
  - Subtitulo: "Tu familia recibira una notificacion para confirmar el traslado."
  - Label monto: "Monto a sumar"
  - Placeholder: "$0"
  - CTA: "Solicitar aporte"
  - Toast confirmacion: "Solicitud enviada. Cuando tu familia lo confirme con su PIN, el dinero llega a tu billetera."

**Vista del padre (notificacion + validacion PIN):**

- **Jerarquia de contenido:**
  1. Titulo personalizado con nombre del hijo y monto
  2. Origen del dinero (producto vinculado del padre)
  3. CTA principal — confirmar con PIN
  4. CTA secundario — ver la billetera de [nombre] antes de confirmar
  5. Aviso legal en una linea al final
- **Componentes sk-*:**
  - `sk-dialog` o `sk-alert` → notificacion de solicitud entrante
  - `sk-inputmask` → campo de PIN (enmascarado)
  - `sk-button` (primary) → "Confirmar con PIN"
  - `sk-button` (secondary) → "Ver la billetera de [nombre]"
  - `sk-confirmdialog` → confirmacion antes de procesar el PIN
- **Microcopy clave padre** *(de skandia-kids-content.md)*:
  - Titulo notificacion: "[Nombre] quiere sumar $[X] a su billetera"
  - Subtitulo: "El dinero saldria de tu cuenta [producto vinculado]."
  - CTA principal: "Confirmar con PIN"
  - CTA secundario: "Ver la billetera de [nombre]"
  - Aviso legal: "Operacion realizada bajo normativa vigente para productos de menores de edad."
- **Restricciones:**
  - 🔴 El aviso legal de una linea en la vista del padre debe ser validado y aprobado por Legal antes de produccion. No puede ser un placeholder.
  - 🟡 Confirmar con Tecnologia el flujo tecnico del PIN: es el PIN del producto Skandia adulto, un PIN nuevo para Kids, o biometria.
- **Transicion:** La vista del adolescente viene de home-adol. La vista del padre viene de la notificacion push. Ambas vistas convergen en el resultado: si el padre aprueba, el saldo del adolescente se actualiza en tiempo real y ambos reciben confirmacion.

---

### Pantalla 07 — Aporte directo del padre (tx-aporte-padre)

- **Actor:** Padre (inicia y valida)
- **Acto:** Acto 2 del Flujo B
- **Job:** El padre aporta directamente a la billetera del hijo sin que el adolescente lo solicite. Requiere su propio PIN.
- **Jerarquia de contenido:**
  1. Titulo con nombre del hijo como destinatario
  2. Monto del aporte
  3. Origen del dinero (producto vinculado)
  4. Confirmacion del impacto en la billetera del hijo
  5. CTA de confirmacion con PIN
  6. Confirmacion de operacion exitosa
  7. Aviso de notificacion al adolescente
- **Componentes sk-*:**
  - `sk-inputnumber` → monto del aporte
  - `sk-select` → selector de cuenta origen (si el padre tiene multiples productos)
  - `sk-inputmask` → campo de PIN
  - `sk-button` (primary) → "Confirmar con PIN"
  - `sk-toast` → confirmacion al padre
  - `sk-messages` → aviso de notificacion enviada al adolescente
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Suma plata a la billetera de [nombre del hijo]"
  - Subtitulo: "El dinero saldra de tu cuenta vinculada. [Nombre] vera el cambio en su billetera."
  - CTA: "Confirmar con PIN"
  - Toast confirmacion: "Listo. Sumaste $[X] a la billetera de [nombre]. El/ella ya puede verlo."
  - Notificacion al adolescente: "Tu familia sumo $[X] a tu billetera. Ya esta disponible."
- **Restricciones:**
  - 🔴 Mismo aviso legal requerido que en tx-aporte — validacion Legal obligatoria antes de produccion.
- **Transicion:** Viene del dashboard parental (home-padre). Va hacia home-padre con el saldo del hijo actualizado.

---

### Pantalla 08 — Solicitar retiro (tx-retiro)

- **Actor dual:** Adolescente (inicia) / Padre (valida con PIN)
- **Acto:** Acto 2 del Flujo A · Acto 2 del Flujo B
- **Job del adolescente:** Retirar de su billetera. El flujo no debe sentirse como pedir permiso — es completar un paso del proceso.
- **Job del padre:** Recibir la solicitud y validar con PIN.

**Vista del adolescente:**

- **Componentes sk-*:** Mismos que tx-aporte con adaptacion de labels
- **Microcopy clave adolescente** *(de skandia-kids-content.md)*:
  - Titulo: "Cuanto quieres retirar?"
  - Subtitulo: "Tu familia confirma el retiro con su PIN. El dinero llega a [destino definido]."
  - CTA: "Solicitar retiro"
  - Toast: "Solicitud lista. Cuando tu familia confirme con PIN, el dinero se procesa."

**Vista del padre:**

- **Microcopy clave padre** *(de skandia-kids-content.md)*:
  - Titulo notificacion: "[Nombre] quiere retirar $[X] de su billetera. Confirma con tu PIN para procesar."
  - CTA: "Confirmar con PIN"
  - Aviso legal: "El retiro se procesa en [X dias habiles] a la cuenta destino vinculada."
- **Restricciones:**
  - 🔴 El plazo de procesamiento del retiro ("[X dias habiles]") debe ser definido por el area de Operaciones antes de produccion.
  - 🔴 Aviso legal de retiro — validacion Legal obligatoria.
  - 🟡 Confirmar la cuenta destino del retiro: va a la cuenta del padre, a una cuenta propia del adolescente, o es configurable.
- **Transicion:** La vista del adolescente viene de home-adol. La vista del padre viene de la notificacion push. Si se aprueba, el saldo del adolescente se actualiza y ambos reciben confirmacion.

---

### Pantalla 09 — Meta cumplida (meta-logro)

- **Actor:** Adolescente (vista principal) + Padre (notificacion push)
- **Acto:** Acto 2 → 3 del Flujo A (momento de transicion)
- **Job:** Celebrar el logro de manera que genere motivacion real y ganas de continuar. Devolver la agencia al adolescente inmediatamente despues de celebrar.
- **Jerarquia de contenido:**
  1. Titulo de celebracion — simple y directo
  2. Nombre de la meta cumplida
  3. Pregunta de agencia: que quieres hacer con esta plata?
  4. CTA de retiro (con aclaracion de aprobacion del equipo)
  5. CTA de nueva meta
  6. Microcopy que recuerda la dinamica de equipo sin cortar la celebracion
- **Componentes sk-*:**
  - `sk-card` → contenedor de celebracion con visual de logro
  - `sk-badge` → insignia de meta cumplida
  - `sk-button` (primary) → "Retirar" (si aplica)
  - `sk-button` (secondary) → "Crear una nueva meta"
  - `sk-button` (tertiary) → "Hacer crecer esta plata" (enlace al Momento 6)
  - `sk-toast` → confirmacion de logro
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Lo lograste!"
  - Subtitulo: "Llegaste a tu meta '[nombre]'. Que quieres hacer con esta plata?"
  - CTA principal: "Retirar"
  - CTA secundario: "Crear una nueva meta"
  - Microcopy retiro: "Para retirar, tu equipo recibira una notificacion para aprobarlo."
  - Notificacion al padre (push): "[Nombre] cumplio su primera meta de ahorro. Ya puede elegir que sigue."
- **Restricciones:**
  - 🟡 Confirmar si la pantalla de meta-logro puede tener un acceso directo a "hacer crecer" como tercer CTA — no superar 2 CTAs principales por pantalla segun restricciones de contenido.
- **Transicion:** Llega automaticamente cuando el progreso de la meta alcanza el 100%. Desde aqui va a tx-retiro (si elige retirar), meta-crear (si elige nueva meta) o crecer-intro (si elige hacer crecer).

---

### Pantalla 10 — Hacer crecer (crecer-intro)

- **Actor:** Adolescente
- **Acto:** Acto 3 del Flujo A
- **Job:** Introducir la diferencia entre guardar y hacer crecer (ahorro vs. inversion) de forma practica, sin clase magistral. El objetivo es curiosidad y apertura — no cierre de venta.
- **Jerarquia de contenido:**
  1. Titulo que sugiere posibilidad sin prometer nada
  2. Analogia simple: guardar quieto vs. hacer trabajar
  3. Aclaracion honesta sobre el riesgo (a veces sube, a veces baja un poco)
  4. Presentacion del rol de Skandia como coach en este momento
  5. CTA de exploracion (no de contratacion)
  6. Microcopy que recuerda que cualquier cambio requiere el equipo
- **Componentes sk-*:**
  - `sk-card` → contenedor de la explicacion con dos estados visuales (guardar vs. hacer crecer)
  - `sk-accordion` → capa 2 de detalle para quien quiere saber mas sin interrumpir el flujo principal
  - `sk-button` (primary) → "Explorar esta opcion"
  - `sk-button` (tertiary) → "Ahora no"
  - `sk-tooltip` → aclaracion de terminos al pasar sobre conceptos nuevos
  - `sk-chip` → etiqueta "Coach Skandia" para identificar al emisor del mensaje
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Tu plata puede hacer mas que esperar."
  - Subtitulo: "Cuando guardas en una meta normal, tu plata espera quieta. Cuando eliges hacerla crecer, trabaja mientras tu haces otras cosas."
  - Capa 2: "No es magia ni es seguro al 100%. A veces sube, a veces baja un poco. Pero con tiempo, tiende a crecer."
  - CTA: "Explorar esta opcion"
  - Opcion secundaria: "Ahora no"
  - Microcopy de equipo: "Cualquier cambio lo aprueba tu equipo."
- **Restricciones:**
  - 🔴 Esta pantalla no puede ir a produccion sin validacion legal del Momento 6 completo. El copy de riesgo exacto depende del producto subyacente (fondo variable, conservador, CDT). Ver decision pendiente en seccion 6.
  - 🟡 La frase "Tu plata puede hacer mas que esperar" debe ser revisada por Legal para confirmar que no activa obligaciones de disclosure bajo normativa de productos de inversion para menores.
- **Transicion:** Llega desde home-adol o desde meta-logro. Va hacia la pantalla de seleccion de producto (fuera del alcance de este PRD — requiere definicion de producto subyacente).

---

### Pantalla 11 — Microreto desbloqueado (reto-unlock)

- **Actor:** Adolescente
- **Acto:** Transversal — aparece durante el Acto 2 del Flujo A cuando el sistema detecta el momento apropiado
- **Job:** Presentar el primer microreto de aprendizaje como parte del juego, no como contenido obligatorio. El reto llega — no se impone.
- **Jerarquia de contenido:**
  1. Indicador de que el reto fue desbloqueado (lenguaje de juego)
  2. Descripcion del reto — concreta, relacionada con su vida real
  3. Recompensa visible por completar el reto
  4. CTA de inicio
  5. Opcion de posponer (siempre hay salida)
  6. Microcopy de privacidad — el reto es solo del adolescente
- **Componentes sk-*:**
  - `sk-card` → contenedor del reto con visual de desbloqueo
  - `sk-badge` → etiqueta de recompensa
  - `sk-button` (primary) → "Empezar reto"
  - `sk-button` (tertiary) → "Mas tarde"
  - `sk-progressbar` → barra de progreso del reto una vez iniciado
  - `sk-chip` → nivel o categoria del reto
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo: "Reto desbloqueado"
  - Descripcion: "Sabes en que se va tu plata cada semana? Registra tus 3 gastos mas grandes de los ultimos 7 dias."
  - Recompensa: "Completa este reto y desbloquea [siguiente funcion / insignia / nivel]"
  - CTA: "Empezar reto"
  - Opcion secundaria: "Mas tarde"
  - Microcopy de privacidad: "Este reto es solo tuyo. No se comparte con tu equipo."
- **Restricciones:**
  - 🟡 Confirmar con UX y negocio si los microretos son privados del adolescente o visibles al padre — esto determina si el microcopy de privacidad es correcto o se elimina.
- **Transicion:** Aparece como overlay o pantalla intermedia cuando se detecta el trigger de desbloqueo. Puede llegar desde home-adol o despues de una accion especifica. Si acepta, va al flujo del reto. Si pospone, regresa a la pantalla anterior.

---

### Pantalla 12 — Dashboard parental (home-padre)

- **Actor:** Padre/cuidador
- **Acto:** Acto 2 del Flujo B — pantalla central del seguimiento
- **Job:** El padre ve en un vistazo como va su hijo, tiene acceso a pendientes de validacion y puede entrar al canal completo del adolescente cuando quiera. Siente que esta presente sin necesitar intervenir constantemente.
- **Jerarquia de contenido:**
  1. Titulo personalizado con nombre del hijo
  2. Alerta prioritaria si hay solicitud de validacion pendiente (aparece primero si existe)
  3. Resumen de metas activas: nombre, porcentaje, monto
  4. Ultimo movimiento registrado
  5. CTA de acceso al canal completo del hijo
  6. Mensaje de tranquilidad si no hay actividad reciente
- **Componentes sk-*:**
  - `sk-alert` → alerta de solicitud de validacion pendiente (nivel warning o info segun urgencia)
  - `sk-card` → tarjeta de resumen por meta activa
  - `sk-progressbar` → progreso visual de cada meta
  - `sk-metergroup` → si hay multiples metas y se quiere un resumen agrupado
  - `sk-button` (primary) → "Ver canal de [nombre]" (acceso completo al espacio del hijo)
  - `sk-button` (secondary) → "Ver solicitud" (cuando hay pendiente)
  - `sk-badge` → indicador de pendientes
  - `sk-tag` → etiqueta de estado por meta
- **Microcopy clave** *(de skandia-kids-content.md)*:
  - Titulo seccion: "Asi va [nombre del hijo]"
  - Subtitulo: "Aqui ves un resumen de sus metas y movimientos. Entra a su canal para ver todo el detalle."
  - Estado de meta: "[Nombre de meta]: [%] completada · [Monto] de [Total]"
  - CTA acceso al canal: "Ver canal de [nombre]"
  - Alerta de solicitud pendiente: "[Nombre] quiere sumar $[X] a '[meta]'. Tienes una solicitud pendiente."
  - CTA validacion: "Ver solicitud"
  - Mensaje sin actividad: "[Nombre] no ha hecho movimientos esta semana. Todo tranquilo."
- **Restricciones:**
  - 🟡 Confirmar el nivel de detalle que el padre puede ver en el resumen: ve monto exacto del saldo del hijo, solo el progreso porcentual de las metas, o ambos. La decision impacta el microcopy y el componente a usar.
- **Transicion:** Accesible desde el portal Skandia del padre (seccion Kids). Desde aqui puede ir al canal completo del hijo, a la pantalla de validacion PIN (tx-aporte o tx-retiro) o a tx-aporte-padre para aportar directamente.

---

## 5. Principios de diseno para este caso

**1. La agencia del adolescente es el diseno.**
Cada decision de arquitectura, cada CTA, cada jerarquia de contenido debe reforzar que el protagonista es el adolescente. El padre esta presente — pero en el diseno del adolescente su presencia se siente como equipo, no como limite. Nada en la experiencia del adolescente debe parecer una pantalla diseñada para sus papas.

**2. Cero friccion innecesaria en el onboarding del adolescente.**
Los hallazgos de Joven Go son directamente aplicables: demasiados clicks, exceso de texto y onboarding largo son las causas documentadas de abandono en el segmento adulto joven. En adolescentes, la tolerancia es aun menor. El diseno debe llevar al adolescente a su primera meta activa en el menor numero de pasos posible. Si algo no es estrictamente necesario para la primera sesion, va despues.

**3. La supervision parental es invisible en la experiencia del adolescente.**
El PIN, las notificaciones al padre, las validaciones: todo existe y es necesario, pero el diseno del flujo del adolescente debe normalizarlos como parte del proceso — nunca como interrupciones ni como recordatorios de que no puede operar solo. El microcopy de Kiki ya lo resuelve en los textos; el diseno visual debe reforzarlo.

**4. La bifurcacion de actor debe ser perfectamente coherente.**
El mismo evento (aporte, retiro, logro) se ve desde dos angulos distintos: el del adolescente y el del padre. La experiencia del padre debe sentirse como la de un adulto que usa Skandia — no como una app de ninos. La coherencia visual y narrativa entre los dos canales es lo que hace que el concepto de equipo funcione en la practica.

---

## 6. Decisiones pendientes antes de produccion

- 🔴 **Legal — Texto exacto del aviso obligatorio en transacciones (aportes y retiros):** No puede ser placeholder en produccion. Afecta pantallas 06, 07 y 08.
- 🔴 **Legal — Copy del Momento 6 (hacer crecer):** El copy de riesgo depende del producto subyacente (fondo variable, conservador, CDT). La pantalla crecer-intro no puede ir a produccion sin esta definicion. Afecta pantalla 10.
- 🔴 **Operaciones — Plazo de procesamiento de retiros:** El "[X dias habiles]" del microcopy del retiro debe reemplazarse con el dato real. Afecta pantalla 08.
- 🟡 **Legal — "Hacer crecer tu plata":** Confirmar que la expresion no activa obligaciones adicionales de disclosure bajo normativa de productos de inversion para menores en Colombia. Afecta pantallas 02 y 10.
- 🟡 **Legal — Mecanismo de PIN:** Confirmar que el lenguaje de validacion parental por PIN esta alineado con los requerimientos legales para operaciones de menores de edad. Afecta pantallas 06, 07 y 08.
- 🟡 **Legal — "Inversiones" en el subtitulo de bienvenida del adolescente:** Revisar si activa obligaciones de disclosure. Afecta pantalla 02.
- 🟡 **Legal — "Coach financiero de Skandia":** Confirmar que el titulo de coach no activa obligaciones bajo normativa de asesoria financiera. Afecta pantalla 03.
- 🟡 **Tecnologia — Endpoint de saldo en tiempo real:** Confirmar disponibilidad y tiempo de actualizacion para el dashboard del adolescente. Afecta pantalla 04.
- 🟡 **Tecnologia — Mecanismo exacto del PIN:** Definir si es el PIN del producto Skandia del adulto, un PIN dedicado para Kids, o biometria. Impacta el diseno del componente en pantallas 06, 07 y 08.
- 🟡 **Tecnologia — Cuenta destino del retiro:** Confirmar si el dinero va a la cuenta del padre, a una cuenta propia del adolescente o es configurable. Afecta pantalla 08.
- 🟡 **Negocio — Productos subyacentes de "hacer crecer":** Definicion de producto requerida antes de poder completar la pantalla 10.
- 🟡 **Negocio/UX — Privacidad de microretos:** Confirmar si los retos del adolescente son visibles al padre o solo del adolescente. Determina el microcopy de privacidad de la pantalla 11.
- 🟡 **Negocio — Nivel de detalle del dashboard parental:** Definir si el padre ve el saldo exacto del hijo o solo el progreso porcentual de las metas. Afecta pantalla 12.
- 🟡 **Research — Sprint de tension autonomia vs. control:** Antes de produccion se recomienda una sesion con padres para explorar cuanta libertad de error estan dispuestos a conceder al hijo. Esto puede impactar los limites de transaccion y los mensajes de validacion.
- 🟡 **Marca — Nombre definitivo del producto:** "Skandia Kids" es el nombre provisional. Definicion del nombre final requerida antes de produccion (opciones recomendadas por Kiki: Skandia Tu, Skandia Avanza, Skandia Base). Impacta todos los titulos del producto.
- 🟡 **Marca — "Plata" vs. "dinero":** Definicion del regionalismo en la voz de Skandia Kids requiere alineacion con el equipo de marca antes de produccion.
- 🟡 **UX — Ejemplos de placeholder de metas:** Los textos "mis tenis, viaje a Santa Marta, mi primer millon" deben validarse con adolescentes reales del segmento antes de produccion. Afecta pantalla 05.

---

## 7. Instruccion a Rachel

- **Entregable esperado:** Prototipo `.html` autocontenido — mobile-first (375px) para las pantallas del adolescente, desktop para el dashboard parental
- **Figma:** Solo si el usuario lo solicita explicitamente
- Consultar `skandia-kids-content.md` para todos los textos de interfaz — el microcopy esta definido por momentos y no debe alterarse sin revision de Kiki
- **Canal principal:** El experimento vive **dentro de la app Skandia existente** (sección dedicada, mobile-first 375px) para el adolescente, y dentro del **portal web Skandia existente** (sección dedicada, desktop) para el padre. El prototipo debe simular esta integración: mostrar el shell de la app/portal actual con la sección Kids dentro, no como producto independiente.
- **Punto de entrada en el prototipo:** Incluir una pantalla de contexto que muestre desde dónde se accede a la sección Kids (ej: tarjeta o ítem de menú dentro de la app Skandia que lleva al flujo del adolescente).
- **Prioridad de prototipado:** Flujo del adolescente completo primero (pantallas 02 a 11), luego el flujo parental (pantallas 01 y 12). Los puntos de intersection (pantallas 06, 07, 08) deben mostrar las dos vistas.
- **Elementos marcados con 🔴** son bloqueantes para produccion — los placeholders en el prototipo estan permitidos, pero deben marcarse visualmente como "pendiente de Legal/Ops" para que no avancen sin resolucion.
- **Tono visual:** La experiencia del adolescente debe sentirse diferente al Skandia adulto en energia y personalidad — pero compartir el sistema de diseno (sk-*). No infantilizar. La experiencia del padre debe sentirse como Skandia adulto con una seccion especializada.
- **Gamificacion:** Los elementos de logro, reto desbloqueado y progreso de meta son el motor visual de la experiencia del adolescente. Deben ser prominentes y energicos sin ser cartoonish.
- La bifurcacion de actor en las pantallas transaccionales (06, 07, 08) debe ser clara — el prototipo debe mostrar las dos vistas de cada transaccion.

---

## 8. Senal de handoff a Kiki (Modo Revisora)

Una vez que Rachel entregue el prototipo, Kiki recibe para revision de microcopy:
- **Canal:** App Skandia mobile-first (adolescente) + Portal web (padre)
- **Segmento:** Adolescentes 13–17 anos (Financial Explorer en formacion) + Padres/cuidadores (Family Guardians)
- **Fuentes de verdad:** skandia-comunicacion + master-de-segmentacion + skandia-kids-content.md
- **Puntos de atencion prioritarios para revision:**
  - Que el tono con el adolescente no sea condescendiente ni infantilice
  - Que el vocabulario del glosario (meta, plata, equipo, hacer crecer, logro, reto) este aplicado consistentemente
  - Que los textos de supervision parental nunca suenen a vigilancia ni a permiso desde la perspectiva del adolescente
  - Que los avisos legales sean minimos, al final de la accion, y no sean protagonistas de ninguna pantalla
  - Que no haya mas de 2 CTAs principales por pantalla
  - Que no se use la palabra "kids" para referir al adolescente dentro de la experiencia

---

*UX Estratega · Skandia Colombia · #UXplorers*
*Fecha: Junio 2026 · Basado en: skandia-kids-research.md + skandia-kids-content.md (aprobados)*
