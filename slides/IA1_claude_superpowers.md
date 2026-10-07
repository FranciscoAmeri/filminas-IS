---
title: Claude y Superpowers
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Claude y Superpowers
#### Agentes de IA aplicados al proceso de software
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---
<!-- .slide: style="font-size: 0.75em" -->
<style>
.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}

.exercise-slide {
  border: 2px dashed #b58900;
  border-radius: 12px;
  padding: 20px;
}

.fuente {
  border-top: 2px solid rgba(121, 177, 217, 0.6);
  padding-top: 8px;
  margin-top: 14px;
  font-size: 0.80em;
}

.alerta {
  border-left: 5px solid #b58900;
  padding-left: 14px;
  text-align: left !important;
}

.term {
  background: rgba(121, 177, 217, 0.18);
  padding: 1px 6px;
  border-radius: 4px;
}
</style>

## Recorrido

<div class="grid-item">

1. **Modelo, agente y herramientas** — el vocabulario
2. **Claude** — qué es y dónde se usa
3. **Skills y plugins** — proceso empaquetado
4. **Superpowers** — un proceso de software impuesto
5. **Práctica** — instalarlo y correr un flujo
6. **Artifacts** — publicar, persistir y hostear
7. **Mirarlo con ojo crítico**

</div>

**La tesis de la clase:** una *skill* no es magia, es **un procedimiento escrito**. Y escribir
procedimientos repetibles es exactamente de lo que viene hablando toda la materia.

---

## 1 · El vocabulario
### Modelo, agente y herramientas

<!-- .slide: style="font-size: 0.80em" -->

Tres palabras que se usan como sinónimos y no lo son:

<div class="grid-item">

**Modelo (LLM)** — predice texto. Entra texto, sale texto. No hace nada más.

**Herramientas (tools)** — funciones que el modelo puede pedir que se ejecuten: leer un archivo,
correr un comando, consultar una API.

**Agente** — un modelo **en un bucle**, con herramientas y un objetivo. Decide, actúa, mira el
resultado y vuelve a decidir, hasta terminar o rendirse.

</div>

**Lo que hace la diferencia no es el modelo, es el bucle.** El mismo modelo que te sugiere una
línea de código, metido en un bucle con acceso al repositorio, puede recorrer un proyecto entero.

----

### Autocompletado vs. agente
<!-- .slide: style="font-size: 0.72em" -->

| | Autocompletado | Agente |
|---|---|---|
| **Qué ve** | El archivo abierto | El repositorio, la consola, los tests |
| **Qué hace** | Propone el próximo fragmento | Lee, edita varios archivos, ejecuta, corrige |
| **Quién decide los pasos** | Vos | El agente, dentro de los límites que le pongas |
| **Unidad de trabajo** | Una línea | Una tarea |
| **El riesgo** | Aceptar una línea mala | Que haga 40 cambios en la dirección equivocada |

El segundo riesgo es cualitativamente distinto, y es el que justifica toda esta clase:
**cuanta más autonomía, más importa el proceso.**

---

## 2 · Claude

<!-- .slide: style="font-size: 0.78em" -->

Claude es la familia de modelos de **Anthropic**. Al momento de esta clase los modelos vigentes son
**Claude Fable 5**, **Claude Opus 5.5**, **Claude Sonnet 5** y **Claude Haiku 4.5**, que se
diferencian en capacidad, velocidad y costo.

El mismo modelo se usa desde productos muy distintos:

<div class="grid-item">

**Chat** — web, móvil y aplicación de escritorio
**API / Claude Platform** — para integrarlo en un sistema propio
**Claude Code** — agente de programación en la terminal
**Claude in Chrome · Claude in Excel** — agentes dentro del navegador y de la planilla
**Cowork** — agente de escritorio para tareas de archivos y automatización

</div>

Para esta clase nos interesa **Claude Code**, porque es donde el proceso de software se vuelve
visible.

----

### Claude Code
<!-- .slide: style="font-size: 0.78em" -->

Es un agente que corre en la **terminal**, dentro de tu proyecto. Con tu permiso puede:

* leer y escribir archivos del repositorio,
* ejecutar comandos (compilar, correr los tests, `git`),
* buscar en la web y leer documentación,
* y hacer *commits*.

<div class="alerta">

**El punto que importa como ingenieros:** nada de eso garantiza que el resultado sea bueno. Un
agente rápido sin método produce deuda técnica rápido. Lo que falta es **proceso** — y ahí entran
las *skills*.

</div>

---

## 3 · Skills y plugins
### Proceso empaquetado

<!-- .slide: style="font-size: 0.72em" -->

| Concepto | Qué es | Analogía en la materia |
|---|---|---|
| <span class="term">Skill</span> | Un archivo **Markdown** con conocimiento, un procedimiento o instrucciones. Claude la carga cuando el caso aplica, o se la invoca con `/nombre` | Un **estándar** o una **plantilla** de la cátedra |
| <span class="term">Agent</span> | Un sub-agente con su propio rol y sus propias herramientas | Delegar en un rol del equipo |
| <span class="term">Hook</span> | Código que se dispara ante un evento (antes de un commit, al editar un archivo) | Un **control automático** del proceso |
| <span class="term">MCP server</span> | Un conector a un sistema externo (Jira, Drive, una base) | Una **integración** |
| <span class="term">Plugin</span> | Un paquete que agrupa skills, agents, hooks y MCP servers, y se instala como una unidad | Un **framework de proceso** |
| <span class="term">Marketplace</span> | Un catálogo de plugins, versionado en un repositorio git | Un **repositorio de componentes** |

----

### Una skill es proceso escrito
<!-- .slide: style="font-size: 0.80em" -->

Una skill es, literalmente, un `.md` con un título, una descripción de **cuándo usarla** y los
pasos a seguir. Nada más.

Eso significa tres cosas que nos tocan de cerca:

<div class="grid-item">

1. **Es legible y auditable.** Podés abrirla y discutir si el procedimiento está bien.
2. **Es versionable.** Vive en un repositorio, con historial y revisiones: **gestión de la
   configuración** aplicada al proceso mismo.
3. **Es reutilizable.** Lo que una persona del equipo hace bien, se escribe una vez y lo hacen todos.

</div>

**Es la vieja idea de la ingeniería de software:** si un procedimiento depende de que alguien se
acuerde, no es un proceso. Es una costumbre.

----

### Los comandos que hay que conocer
<!-- .slide: style="font-size: 0.70em" -->

| Para | Comando |
|---|---|
| Abrir el panel de plugins | `/plugin` |
| Instalar uno del catálogo oficial | `/plugin install <nombre>@claude-plugins-official` |
| Agregar otro catálogo | `/plugin marketplace add <owner>/<repo>` |
| Listar lo instalado | `claude plugin list` *(desde la terminal)* |
| Recargar tras instalar | `/reload-plugins` |

Al instalar hay que elegir un **alcance**, y la decisión es de configuración, no de gusto:

* **user** — para vos, en todos tus proyectos
* **project** — para todo el equipo; la entrada se **commitea** en `.claude/settings.json`
* **local** — para vos, solo en este repositorio

<div class="fuente">

📎 Documentación: [Install and manage plugins](https://code.claude.com/docs/en/discover-plugins) ·
[Plugins overview](https://docs.claude.com/en/docs/claude-code/plugins) ·
[Artifacts](https://code.claude.com/docs/en/artifacts)

</div>

---

## 4 · Superpowers

<!-- .slide: style="font-size: 0.80em" -->

Plugin creado por **Jesse Vincent**, de licencia **MIT**, distribuido en el marketplace oficial de
Anthropic.

No agrega capacidades nuevas al modelo. Hace algo distinto y más interesante:
**le impone un proceso de desarrollo.**

<div class="grid-item">

**Primero** entiende el problema y escribe un diseño.
**Después** convierte el diseño en un plan de tareas verificables.
**Recién entonces** escribe código, con TDD y revisión entre tareas.

</div>

Dicho de otro modo: toma un agente que tiende a tirarse de cabeza a codificar y lo obliga a
**analizar, diseñar y planificar antes**.

----

### El ciclo de vida, skill por skill
<!-- .slide: style="font-size: 0.62em" -->

| Etapa del proceso | Módulo de la materia | Skill |
|---|---|---|
| Elicitación y análisis | II — Requisitos | `brainstorming` |
| Especificación | II — Requisitos | el **spec** que deja escrito en `docs/` |
| Planificación | IV — Gestión de proyectos | `writing-plans` |
| Implementación | III — Diseño | `executing-plans` · `subagent-driven-development` |
| Pruebas | V — Calidad | `test-driven-development` · `verification-before-completion` |
| Revisión técnica | V — Calidad | `requesting-code-review` · `receiving-code-review` |
| Depuración | V — Mantenimiento | `systematic-debugging` |
| Gestión de la configuración | V — Configuración | `using-git-worktrees` · `finishing-a-development-branch` |

**Mirá la columna del medio.** No es casualidad: el plugin es una implementación de un proceso de
desarrollo clásico. **Todo lo que vimos en el año está en esa tabla.**

----

### La regla central: el *hard gate*
<!-- .slide: style="font-size: 0.76em" -->

La skill de `brainstorming` clasifica cualquier pedido en uno de tres caminos, y cada uno exige una
aprobación distinta **antes** de tocar código:

| Camino | Cuándo | Qué hay que aprobar primero |
|---|---|---|
| **Spike** | Una pregunta de factibilidad: *"¿se puede…?"* | La pregunta y la prueba, en 2 o 3 oraciones |
| **Bounded** | Un cambio acotado sobre código que **ya existe** | Un diseño corto, conversado |
| **Architectural** | Proyecto nuevo o cambio estructural | Un **spec escrito** y después un **plan escrito** |

Y la regla que lo sostiene: **ante la duda entre dos caminos, se toma el más pesado**, y la
clasificación solo puede subir, nunca bajar.

**Por qué esto es lo más valioso del plugin:** es la respuesta de ingeniería al problema del
agente autónomo. No se trata de que escriba mejor código, sino de que **no escriba código
todavía**.

----

### Lo que esto previene
<!-- .slide: style="font-size: 0.72em" -->

| Sin proceso | Con el gate |
|---|---|
| *"Hacé un sistema de reservas"* → 2.000 líneas en una dirección que no era | Se discute el alcance primero y se aprueba un diseño de media página |
| Se arregla el síntoma del bug | `systematic-debugging` prohíbe el fix sin causa raíz |
| *"Listo, funciona"* sin haberlo corrido | `verification-before-completion` exige **evidencia antes de la afirmación** |
| Tests escritos después, si hay tiempo | `test-driven-development` impone rojo → verde → refactor |
| Todo en `main` | `using-git-worktrees` aísla el trabajo |

La frase que resume la filosofía del plugin: **evidencia antes de afirmaciones.** Es la misma idea
que la verificación y validación del Módulo V.

---

## 5 · Práctica
### Instalación

<!-- .slide: style="font-size: 0.72em" -->

**Requisitos:** Node.js, `git`, y una cuenta de Claude.

```bash
# 1. Instalar Claude Code
npm install -g @anthropic-ai/claude-code

# 2. Entrar al proyecto y arrancar
cd mi-proyecto
claude
```

Ya dentro de la sesión:

```text
/plugin install superpowers@claude-plugins-official
```

Se abre el panel con el detalle del plugin: **leelo antes de aceptar** — ahí dice qué skills,
agentes y hooks agrega, y cuánto contexto consume. Elegís el alcance y, si lo pide,
`/reload-plugins`.

**Verificación:** escribí `/` y buscá las entradas `superpowers:`. Si aparecen, quedó activo.

----

### El flujo, con un ejemplo de la materia
<!-- .slide: style="font-size: 0.66em" -->

Supongamos que el pedido es *"agregar al portal de entradas la devolución hasta 48 horas antes"*.

<div class="grid-item">

**1 · `/superpowers:brainstorming`** → clasifica el pedido. Hay código existente y el cambio es
acotado: **bounded**. Pregunta de a una: ¿la devolución es total o parcial? ¿Qué pasa con las
butacas? ¿Quién la autoriza?

**2 ·** Presenta un **diseño corto** y **se detiene**. No escribe nada hasta que digas que sí.

**3 · `writing-plans`** *(si fuera architectural)* → convierte el diseño en tareas verificables.

**4 · `test-driven-development`** → escribe primero el test que falla: *"una devolución pedida a
47 horas se rechaza"*.

**5 · `requesting-code-review`** → un sub-agente revisa y clasifica los hallazgos por severidad.

**6 · `finishing-a-development-branch`** → cierra la rama.

</div>

**Lo que hay que notar:** entre el paso 1 y el paso 4 **no se escribió una sola línea de código**.

---

### 💡 Ejercicio: Clasificar los pedidos
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.72em" -->

Para cada pedido, decidí si es **spike**, **bounded** o **architectural**, y qué habría que
aprobar antes de escribir código:

1. *"Corregir el mensaje de error cuando el QR ya fue usado."*
2. *"¿Se podría leer el QR con la cámara del celular sin instalar una app?"*
3. *"Agregar un módulo de abonos para varias funciones."*
4. *"Cambiar el límite de 6 entradas a 4."*
5. *"Migrar el portal a microservicios."*

<!--
1. Bounded. El flujo existe, se lee y se cambia. Diseño corto en el chat.
2. Spike. Es una pregunta de factibilidad: la salida es una respuesta, no codigo. Lo que se
   construya queda etiquetado como descartable.
3. Architectural. Toca el modelo de dominio (que es un abono: compra, entrada o entidad nueva),
   los precios y la devolucion. Spec escrito y despues plan escrito.
4. Trampa. Parece trivial, y por eso es el caso mas interesante: si el 6 esta hardcodeado en un
   solo lugar es bounded; si esta repetido en tres capas, la complejidad oculta SUBE el camino y
   hay que parar y decirlo. La regla es que la clasificacion solo sube.
5. Architectural, y ademas demasiado grande para un solo spec: hay que descomponerlo en
   sub-proyectos antes de disenar nada.
-->

---

## 6 · Artifacts
### Del agente a una página publicada

<!-- .slide: style="font-size: 0.78em" -->

Un **artifact** es una página web interactiva que el agente **publica** desde la sesión a una URL
en claude.ai. Se abre en el navegador y **se actualiza en el lugar** mientras la sesión sigue.

Sirve cuando el texto de la terminal es el medio equivocado: un tablero, un diff anotado, varias
alternativas de diseño lado a lado, una checklist que se va completando sola.

<div class="alerta">

**Lo que un artifact no es: un despliegue.** Es una **captura de trabajo** — una sola página
autocontenida, sin backend y sin rutas. Para una herramienta interna de verdad, hosting propio.

</div>

----

### Cómo funciona por dentro
<!-- .slide: style="font-size: 0.64em" -->

El agente escribe un archivo `.html`, `.htm` o `.md`. Claude Code lo **envuelve en un documento
HTML** y lo sirve bajo una **Content Security Policy estricta**, desde un origen aislado
(`*.claudeusercontent.com`) **distinto** del de claude.ai.

Esa CSP es la que define qué puede hacer la página:

| Restricción | Efecto concreto |
|---|---|
| **Pedidos externos** | Tipografías solo de Google Fonts. Scripts solo de **5 CDN** (cdnjs, unpkg, Tailwind, jQuery, jsDelivr). **Imágenes externas bloqueadas.** `fetch`, XHR y WebSocket solo al propio origen |
| **Sin backend** | Página estática. **No puede autenticar visitantes** |
| **Una sola página** | Los enlaces relativos **no resuelven**: no hay nada desplegado al lado |
| **Descargas** | La página no puede iniciar una descarga por su cuenta |
| **Tamaño** | La página renderizada, máximo **16 MiB** |

<div class="alerta">

**Leelo como ingeniero:** la CSP es un **requisito no funcional** que determina el diseño. Por eso
el agente *inlinea* todo el CSS y el JS y mete las imágenes como `data:` URI. No es una decisión
de estilo — **es la arquitectura la que la impone.**

</div>

----

### El despliegue y las versiones
<!-- .slide: style="font-size: 0.74em" -->

<div class="grid-item">

1. El agente escribe el archivo y lo **publica**. Imprime la URL y abre el navegador.
2. **Cada publicación es una versión.** Desde el control *Share* elegís cuál ve el visitante.
3. Actualizar = **republicar a la misma URL**. Quien la tenga abierta lo ve en el lugar.
4. Nace **privado**. Se comparte dentro de la organización o públicamente; en Team y Enterprise el
   compartido público lo habilita un *Owner*.
5. `/artifacts` lista los propios y los compartidos con vos.

</div>

**Gestión de la configuración, aplicada:** versionado, control de acceso por audiencia, registro de
auditoría y política de retención. Es el Módulo V funcionando sobre una página web.

----

### ¿Dónde viven los datos?
<!-- .slide: style="font-size: 0.62em" -->

La pregunta tiene **tres respuestas distintas** que se confunden todo el tiempo:

| Qué | Dónde vive | Quién lo ve | Cuánto dura |
|---|---|---|---|
| **El contenido de la página** | Infraestructura de Anthropic, **versionado** | Según la audiencia que elegiste | Hasta que la borres o venza la retención |
| **Los datos que muestra** | *(a)* **embebidos** en el HTML al publicar — una foto del momento<br>*(b)* traídos **en vivo** por conectores MCP al abrirla | *(a)* todos ven lo mismo<br>*(b)* cada uno ve lo suyo | *(a)* congelados<br>*(b)* se refrescan |
| **Lo que escribe el visitante** | El **navegador del visitante** | Solo él | Puede desaparecer |

<div class="alerta">

**No hay base de datos.** Si dos visitantes tienen que ver lo mismo que uno de ellos cargó,
**un artifact no alcanza.** Ese es el límite, y es arquitectónico, no una función que falte.

</div>

----

### Los conectores: autorización delegada
<!-- .slide: style="font-size: 0.70em" -->

Una página estática no puede hacer `fetch` a cualquier host — la CSP lo prohíbe. Entonces, ¿cómo
trae datos en vivo? **No los trae ella: los pide a claude.ai, que hace la llamada.**

Y acá está lo interesante como diseño de seguridad:

<div class="grid-item">

* La llamada corre con **la cuenta del que mira**, no la del que publicó.
* Dos personas abren el mismo tablero y **pueden ver datos distintos**.
* El visitante **aprueba el acceso** la primera vez.
* **La página nunca ve las credenciales.** claude.ai hace la llamada por ella.
* El que publica **declara** qué conectores puede usar la página, y no puede salirse de ahí.

</div>

Es el patrón de **autorización delegada con declaración previa de permisos**: el mismo problema que
resuelven OAuth o los *scopes* de una API. Vale la pena mirarlo porque es un ejemplo real y chico.

----

### 💡 Hostearlo vos mismo: tres niveles
<!-- .slide: style="font-size: 0.60em" -->

**Nivel 1 — Sitio estático.** La página **ya es** un HTML autocontenido. Lo bajás y lo subís a
cualquier hosting estático. **Ya sabés hacerlo: es exactamente lo que hacemos con estas filminas.**

```bash
cp mi_artifact.html docs/index.html
git add . && git commit -m "publicar" && git push
# GitHub -> Settings -> Pages -> Source: la rama
```

Sirve igual Cloudflare Pages, Netlify, Vercel o un `nginx` propio.

| Ganás | Perdés |
|---|---|
| Tu dominio · sin CSP ajena · imágenes y librerías de donde quieras · varias rutas y varias páginas | **Los conectores MCP dejan de funcionar** (esas llamadas las hacía claude.ai) · el versionado y el control de acceso · el visor |

**Nivel 2 — Persistencia real.** Para que lo que carga un visitante lo vea otro hace falta
**backend**: un *backend-as-a-service* (Supabase, Firebase) o uno propio con su base.

**Nivel 3 — Autenticación.** Cloudflare Access, Netlify Identity o un *proxy* con OAuth adelante.

<div class="alerta">

**El salto del nivel 1 al 2 no es un detalle de implementación: es un cambio de arquitectura.**
Pasás de una página a un sistema cliente-servidor, con autenticación, autorización, validación del
lado del servidor y migraciones de datos.

</div>

----

### Artifact o hosting propio
<!-- .slide: style="font-size: 0.66em" -->

| | **Artifact** | **Hosting propio** |
|---|---|---|
| Tiempo hasta publicar | Segundos, desde la sesión | Minutos u horas |
| Dominio | De claude.ai | El tuyo |
| Backend y base de datos | No | Sí |
| Autenticación propia | No | Sí |
| Versionado y control de acceso | Incluido | Lo armás vos |
| Datos en vivo | Conectores del **visitante** | Tu API |
| Mantenimiento | Casi nulo | Tuyo |

**La regla para decidir:** **artifact para comunicar, hosting propio para operar.** Si el objetivo
es que alguien *mire algo y decida*, artifact. Si el objetivo es que alguien *trabaje ahí todos los
días*, hosting propio.

----

### 💡 Ejercicio: ¿Artifact o hosting propio?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.70em" -->

Para cada caso, decidí qué corresponde y **justificá con una restricción concreta**:

1. Mostrarle al cliente tres propuestas de pantalla para que elija una.
2. Que la recepcionista del club cargue las inscripciones todos los días.
3. Un tablero del estado de los tests que el equipo mira en la reunión diaria.
4. El sitio público del portal de entradas, con la compra incluida.
5. Un informe del avance del TP para entregar a la cátedra.

<!--
1. Artifact. Es comunicar para decidir, y se descarta despues. Perfecto.
2. Hosting propio. Los datos tienen que persistir y ser compartidos: no hay backend en un
   artifact. Es el limite duro.
3. Artifact, y es el mejor caso de conector MCP: cada uno lo abre con su cuenta y se refresca
   solo. Ojo que si alguien no tiene el conector, ve la pagina sin la parte viva.
4. Hosting propio, sin discusion: necesita autenticacion, pagos, multiples rutas y un dominio
   propio. Un artifact no puede autenticar visitantes.
5. Artifact. Una pagina, se comparte por link, versionada. Y si la catedra la quiere en PDF,
   se exporta.
-->

---

## 7 · Con ojo crítico
<!-- .slide: style="font-size: 0.70em" -->

<div class="alerta">

**No verifica por vos.** Puede decir que los tests pasan sin haberlos corrido. Por eso existe
`verification-before-completion`, y por eso **vos** mirás la salida de los comandos.

**Puede alucinar.** Inventa APIs, funciones y citas con total seguridad. Todo dato verificable hay
que verificarlo.

**El contexto cuesta.** Cada plugin suma tokens a cada mensaje. El panel muestra el costo: hay que
elegir, no instalar todo.

**La responsabilidad profesional no se delega.** Firmás vos. Un agente no es un coautor al que se
le pueda atribuir un defecto.

**Datos de terceros y credenciales, nunca.** Es un sistema externo: aplican las mismas reglas que
para cualquier integración.

</div>

----

### Lo que sí cambia
<!-- .slide: style="font-size: 0.78em" -->

No es que el ingeniero deje de hacer falta. Cambia **dónde** está su valor:

<div class="grid-item">

**Baja de valor** — escribir el código rutinario, recordar la sintaxis, el *boilerplate*.

**Sube de valor** — saber qué hay que construir, **decidir la arquitectura**, revisar
críticamente, y **reconocer cuándo el resultado está mal**.

</div>

Fijate que las tres que suben son análisis, diseño y verificación. Es decir: **esta materia**.

Para revisar críticamente lo que produce un agente, hay que saber UML, hay que saber qué es una
composición y hay que saber qué es un caso de prueba. Si no, no hay revisión: hay aceptación.

---

### Antes de usarlo en un trabajo, revisá
<!-- .slide: style="font-size: 0.76em" -->

* ¿Entendés **el problema** mejor que el agente? Si no, no estás en condiciones de aprobar su diseño.
* ¿**Leíste** el diseño y el plan antes de decir que sí, o apretaste *enter*?
* ¿**Corriste** los tests vos mismo y viste la salida?
* ¿Podés **explicar** cada decisión del código como si la hubieras tomado vos? *(Porque la tomaste: la aprobaste.)*
* ¿Está claro en el repositorio **qué se generó con asistencia**?
* ¿Hay datos sensibles o de terceros en lo que le pasaste?

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
