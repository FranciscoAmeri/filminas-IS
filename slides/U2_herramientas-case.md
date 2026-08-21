---
title: Herramientas CASE
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Herramientas CASE
Created by <i class="fab fa-telegram"></i>
[edme88]("https://t.me/edme88")

---
<!-- .slide: style="font-size: 0.60em" -->
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
</style>
## Temario
<div class="grid-item">

### Herramientas CASE
* Definición y alcance
* Qué automatizan
* Entornos de desarrollo integrados (IDE)
* Objetivos
* Ventajas y desventajas
* Características que debe soportar
* Clasificaciones
  * Por cobertura del ciclo de vida
  * Por grado de integración
  * Por función
* Funciones de un sistema CASE
* Herramientas en uso hoy
* La IA generativa como herramienta CASE
* De "CASE" a "toolchain"
</div>

---

### ¿Qué son las herramientas CASE?

Para llevar adelante los proyectos de desarrollo de software, y apoyar las actividades del proceso,
se emplea una serie de herramientas denominadas **CASE**.

CASE son las siglas de *Computer-Aided Software Engineering*: **ingeniería de software asistida por
computadora**.

---

### ¿Qué son las herramientas CASE?
<!-- .slide: style="font-size: 0.90em" -->

Son aplicaciones que ayudan a desarrollar software **automatizando tareas** del proceso y brindando
información sobre el sistema que se está construyendo.

Dan soporte a actividades de análisis, diseño, generación de código, pruebas y mantenimiento.

Incluyen editores de diseño, diccionarios de datos, compiladores, depuradores y herramientas de
construcción del sistema, entre muchas otras.

---

### ¿Qué actividades se automatizan?
<!-- .slide: style="font-size: 0.85em" -->

- Desarrollo de **modelos gráficos** del sistema, como parte de la especificación de requerimientos
  o del diseño.
- **Generación de código** a partir de esos modelos.
- Producción de **interfaces de usuario** a partir de una descripción gráfica creada de manera interactiva.
- **Depuración** del programa, suministrando información sobre un programa en ejecución.
- **Traducción automatizada** de programas escritos en una versión anterior de un lenguaje hacia una
  versión más reciente.

---

### Entornos de desarrollo integrados (IDE)
<!-- .slide: style="font-size: 0.90em" -->

Muchas de estas herramientas pueden combinarse en un mismo marco de trabajo llamado **IDE**
(*Integrated Development Environment*, entorno de desarrollo integrado).

Un IDE ofrece un conjunto común de facilidades que las herramientas usan para **comunicarse entre sí
y operar de forma integrada**: el editor, el compilador, el depurador y el control de versiones
comparten el mismo proyecto y los mismos archivos.

**Ejemplos actuales:** Visual Studio Code, IntelliJ IDEA, Eclipse, Visual Studio, Android Studio.

---

### Objetivos de las herramientas CASE
<!-- .slide: style="font-size: 0.85em" -->

1. **Aumentar la productividad** de las áreas de desarrollo y mantenimiento.
2. **Mejorar la calidad** del software producido.
3. **Reducir tiempo y costo** de desarrollo y de mantenimiento.
4. Mejorar la **planificación y el seguimiento** de los proyectos.
5. **Automatizar** tareas repetitivas: documentación, generación de código, chequeo de errores,
   dibujo de diagramas.
6. Favorecer la **reutilización**, la **portabilidad** y la **estandarización de la documentación**.
7. Acumular el **conocimiento de la organización** en un repositorio común, reutilizable en proyectos futuros.
8. Facilitar la aplicación de las distintas **metodologías** propias de la ingeniería de software.

---

### Ventajas
<!-- .slide: style="font-size: 0.85em" -->

- Automatizan tareas tediosas y propensas a error: dibujar diagramas, generar código repetitivo,
  mantener la documentación al día.
- **Garantizan la consistencia**: verifican que todos los elementos del modelo se usen y que no haya
  identificadores duplicados o referencias colgadas.
- Detectan errores **en etapas tempranas**, cuando corregirlos todavía es barato.
- Permiten pasar del modelo al código y del código al modelo, facilitando el mantenimiento.
- Centralizan la información del proyecto, de modo que todo el equipo trabaja sobre la misma versión.

---

### Desventajas
<!-- .slide: style="font-size: 0.85em" -->

- **Dependencia de la metodología**: muchas herramientas imponen un método de trabajo determinado,
  y el equipo termina adaptándose a la herramienta en lugar de al revés.
- **Falta de estándares** entre fabricantes: cada producto usa su propio formato, y migrar de una
  herramienta a otra es caro o directamente imposible.
- **Costo** de adquisición, licencias y capacitación.
- **Curva de aprendizaje**: hasta dominarla, la herramienta hace más lento al equipo.
- **Modelos que nadie mantiene**: si los diagramas dejan de reflejar el código, estorban más de lo
  que ayudan.
- **Funcionalidad limitada** frente a necesidades muy específicas de un proyecto.

----

### 💡 Ejercicio: ¿Conviene la herramienta?
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

En cada situación, decidan si **conviene o no** incorporar la herramienta, y **qué desventaja**
de las vistas pesa más:

1. Un equipo de 3 personas, con dos semanas de plazo, evalúa comprar una suite de modelado que
   requiere una capacitación de 40 horas. <!--No conviene: curva de aprendizaje + costo. El plazo no permite amortizar la inversión.-->
2. Una empresa con 200 desarrolladores quiere unificar cómo se documentan los sistemas. <!--Conviene: el costo se amortiza y el beneficio de la estandarización crece con el tamaño del equipo.-->
3. Un estudio contable pide una herramienta que genere el código a partir de los diagramas, pero
   su sistema tiene reglas fiscales muy particulares. <!--Riesgo de funcionalidad limitada: la generación automática rara vez cubre reglas de negocio específicas; probablemente haya que escribirlas a mano igual.-->
4. Un equipo mantiene diagramas UML en una herramienta que nadie abre desde hace ocho meses. <!--No conviene sostenerla: modelos desactualizados estorban más de lo que ayudan. O se integran al flujo de trabajo, o se abandonan.-->

<!--
Cierre: la pregunta correcta nunca es "¿esta herramienta es buena?" sino "¿es buena para este
equipo, este proyecto y este plazo?". El costo de una CASE no es la licencia: es el tiempo del equipo.
-->

---

### Características que debe soportar
<!-- .slide: style="font-size: 0.85em" -->

- **Soporte gráfico** para distintas técnicas de modelado: DFD, entidad-relación, diagramas de
  transición de estados, modelos orientados a objetos.
- **Control de consistencia**: unicidad de los identificadores, cumplimiento de las reglas de la
  metodología, detección de elementos definidos pero no utilizados.
- **Validación entre modelos**, tanto dentro de una misma fase (por ejemplo, entre el DFD y el
  entidad-relación) como entre fases distintas (el DFD de análisis contra el de diseño).

---

### Características deseables
<!-- .slide: style="font-size: 0.85em" -->

- Soporte **multiusuario**, para que varias personas trabajen sobre el mismo modelo.
- **Personalización** de plantillas, notaciones y reglas.
- **Control de documentos y versiones**.
- **Gestión de proyectos**: planificación y seguimiento.
- **Métricas** de productividad y calidad del software.
- Soporte de **pruebas**, **simulación** y **prototipado**.
- Posibilidad de **verificar** que el software cumple con las especificaciones.
- **Generación de código** a partir de los modelos.

---

### Principales usuarios
- Organizaciones y empresas de desarrollo
- Analistas funcionales
- Desarrolladores
- Ingenieros de software

---

<!--https://tpsis324.blogspot.com/2008/09/3-clasificacion.html-->
### Clasificación de las herramientas CASE
<!-- .slide: style="font-size: 0.90em" -->

No existe una única clasificación. Las tres más usadas responden a preguntas distintas:

| Criterio | La pregunta que responde |
|---|---|
| **Cobertura del ciclo de vida** | ¿Qué fases del proceso cubre? |
| **Grado de integración** | ¿Qué tan acopladas están entre sí? |
| **Función** | ¿Qué tarea concreta resuelve? |

Una misma herramienta se ubica en las tres a la vez: no son alternativas, son puntos de vista.

---

### 1. Por cobertura del ciclo de vida
<!-- .slide: style="font-size: 0.85em" -->

- **Upper CASE** (nivel alto) — Cubren las fases iniciales: planificación, análisis y diseño.
  Trabajan con modelos y diagramas, lejos del código.
- **Lower CASE** (nivel bajo) — Cubren las fases finales: implementación, pruebas y mantenimiento.
  Trabajan sobre el código.
- **I-CASE** (*Integrated CASE*) — Abarcan **todo** el ciclo de vida de forma integrada, conectando
  los modelos del análisis con el código generado.

**Ojo:** *I-CASE* e *Integrated CASE* son lo mismo. La I es de *Integrated*.

----

![Herramientas Case](images/unidad2/herramientas-case.png)

---

### 2. Por grado de integración
<!-- .slide: style="font-size: 0.80em" -->

- **Toolkit** (juego de herramientas) — Conjunto de herramientas que automatizan **una** fase del
  ciclo de vida. Comparten la base de datos de soporte y la interfaz de usuario.
  *Integración baja.*
- **Workbench** (banco de trabajo) — Automatizan **más de una** fase, típicamente análisis + diseño +
  implementación, con la documentación asociada. Además de compartir base de datos e interfaz, están
  basadas en una misma metodología. *Integración media.*
- **IPSE** (*Integrated Project Support Environment*) — Cubren todo el ciclo de vida más la gestión
  del proyecto y de la configuración. *Integración alta.*

El término IPSE es de los años 80 y 90. Hoy su lugar lo ocupan las **plataformas de desarrollo**
como GitHub, GitLab o Azure DevOps, que integran código, seguimiento, pruebas y despliegue.

---

### 3. Por función
<!-- .slide: style="font-size: 0.90em" -->
Según la tarea que resuelven:

1. Planificación de sistemas de gestión
2. Análisis y diseño
3. Programación
4. Integración y prueba
5. Gestión de prototipos
6. Mantenimiento
7. Gestión de proyectos
8. Soporte

----

#### 1. Herramientas de planificación de sistemas de gestión
Sirven para modelar los requisitos de información estratégica de una organización. Proporcionan un
"metamodelo" del cual se pueden derivar sistemas de información específicos. Su objetivo es ayudar a
comprender cómo se mueve la información entre las distintas unidades organizativas.

Son especialmente útiles cuando se diseñan nuevas estrategias de sistemas, o cuando los métodos y
sistemas actuales no satisfacen las necesidades de la organización.

----

#### 2. Herramientas de análisis y diseño
Permiten crear un modelo del sistema que se va a construir y evaluar su validez y consistencia.
Ayudan a detectar errores con anticipación. Incluyen:

- Herramientas de modelado.
- Herramientas de creación de prototipos y de simulación.
- Herramientas para el diseño y desarrollo de interfaces.

----

#### 3. Herramientas de programación
Se engloban aquí los compiladores, editores y depuradores de los lenguajes de programación. Incluyen:

- Herramientas de codificación convencionales.
- Herramientas de programación orientada a objetos.
- Generadores de código a partir de modelos.

----

#### 4. Herramientas de integración y prueba
Dan soporte a la ejecución, medición y verificación del software desarrollado. Entre las más
utilizadas están:

- Herramientas de **análisis estático** del código (detectan defectos sin ejecutarlo).
- Herramientas de **prueba automatizada** (ejecutan las pruebas y reportan los fallos).
- **Generadores de datos** de prueba.
- Herramientas de **cobertura**, que miden qué porción del código fue realmente ejercitada.

----

#### 5. Herramientas de gestión de prototipos
Los prototipos se utilizan ampliamente para evaluar las especificaciones de un sistema, o para
entender mejor cómo los requisitos se ajustan a los objetivos perseguidos.

Estas herramientas permiten construir versiones preliminares navegables sin escribir el sistema
definitivo.

----

#### 6. Herramientas de mantenimiento
Se subdividen en:

- Herramientas de **ingeniería inversa**: reconstruyen los modelos a partir del código existente.
- Herramientas de **reestructuración y análisis de código**.
- Herramientas de **reingeniería**: rehacen el sistema conservando su funcionalidad.

----

#### 6.b. Mantenimiento en producción
<!-- .slide: style="font-size: 0.80em" -->

La clasificación clásica se detiene en el código. Pero hoy buena parte del mantenimiento ocurre
**con el sistema andando**, y hay tres familias de herramientas para eso:

- **Observabilidad y monitoreo** — Registran qué pasa en producción: errores, tiempos de respuesta,
  caídas. Permiten enterarse de un fallo antes de que lo reporte el usuario.
  *Sentry, Grafana, Datadog, Prometheus.*
- **Calidad de código** — Analizan el código de forma estática y bloquean la integración si no
  cumple los umbrales acordados: complejidad, duplicación, cobertura de pruebas.
  *SonarQube, ESLint, Checkstyle.*
- **Seguridad de dependencias** — Avisan cuando una librería que usa el proyecto tiene una
  vulnerabilidad conocida, y muchas veces proponen la actualización automáticamente.
  *Dependabot, Snyk, npm audit.*

Todas encajan en la definición de CASE: automatizan una actividad del proceso y brindan
información sobre el software.

----

#### 7. Herramientas de gestión de proyectos
Se centran en aspectos específicos de la gestión, en lugar de dar un soporte global. Con un conjunto
adecuado se puede estimar esfuerzo, costo y duración, hacer un seguimiento continuo del proyecto y
medir productividad y calidad.

Se incluyen:

- Herramientas de planificación de proyectos.
- Herramientas de seguimiento de requisitos, que permiten rastrear un requisito desde el pliego
  inicial hasta el producto final.
- Herramientas de gestión y medición.

----

#### 8. Herramientas de soporte
Recogen actividades aplicables a **todo** el proceso de desarrollo:

- Herramientas de documentación.
- Herramientas para software de sistemas.
- Herramientas de control de calidad.
- Herramientas de bases de datos.

---

### Funciones de un sistema CASE
<!-- .slide: style="font-size: 0.85em" -->

Además de clasificarlas, conviene distinguir las **cinco funciones** que un sistema CASE puede
ofrecer. No son categorías excluyentes: **un mismo producto suele ofrecer varias a la vez.**

1. **Repositorio**
2. **Reingeniería**
3. **Soporte del ciclo de vida**
4. **Soporte de proyecto**
5. **Mejora continua de la calidad**

----

#### 1. Repositorio
Los sistemas CASE funcionan en torno a un **repositorio central**, que contiene todas las
definiciones de objetos y sus relaciones: diagramas de flujo de datos, diagramas entidad-relación,
esquemas de bases de datos, diseños de pantallas.

Es el núcleo que **soporta a las otras cuatro funciones**. Todo sistema CASE tiene un repositorio
propio o trabaja sobre uno provisto por otro fabricante.

----

#### 2. Reingeniería
Los sistemas CASE permiten establecer una relación formal entre los productos generados en las
distintas fases del ciclo de vida, y recorrerla en los dos sentidos:

- **Ingeniería directa:** de las especificaciones al código.
- **Ingeniería inversa:** del código a las especificaciones.

Al conjunto de ambas se lo denomina **reingeniería**. Esto permite hacer una modificación en la fase
más adecuada y propagarla a las demás.

----

#### 3. Soporte del ciclo de vida
El ciclo de vida de un sistema se compone de varias etapas. De modo simplificado:

- Planeamiento
- Análisis y diseño
- Implantación (programación y pruebas)
- Mantenimiento y actualización

Un sistema CASE puede cubrirlas todas, o especializarse en algunas: es la distinción entre
**Upper CASE** (las dos primeras) y **Lower CASE** (las dos últimas) que vimos antes.

----

#### 4. Soporte de proyecto
Da soporte a las actividades que surgen del **trabajo en grupo** durante el desarrollo: facilidades
de comunicación, creación e intercambio de documentación, herramientas personales, control de
accesos y de seguridad.

Los sistemas CASE le dan a esto una importancia muy variable, por lo cual el soporte de proyecto
suele ser un factor de diferenciación entre productos.

----

#### 5. Mejora continua de la calidad
Los sistemas CASE se asocian habitualmente a la productividad, pero una de sus principales ventajas
está en la **calidad** de los desarrollos.

Algunos productos enfatizan este punto más que el de la productividad, incorporando herramientas
que permiten ejercer un control de garantía de calidad **desde las primeras fases** del ciclo de
vida, y no solamente al final.

---

### Herramientas CASE en uso hoy
<!-- .slide: style="font-size: 0.62em" -->

Casi todo lo que usan a diario es una herramienta CASE, aunque nadie las llame así:

| Función | Herramientas |
|---|---|
| Modelado y diseño | StarUML, Enterprise Architect, draw.io, PlantUML, Lucidchart |
| Modelado de datos | ERwin, PowerDesigner, MySQL Workbench, DBeaver |
| Desarrollo (IDE) | VS Code, IntelliJ IDEA, Eclipse, Visual Studio |
| Control de versiones | Git, GitHub, GitLab |
| Pruebas | JUnit, Jest, Selenium, Postman |
| Integración y despliegue | GitHub Actions, Jenkins, Docker |
| Gestión del proyecto | Jira, Trello, Azure DevOps |
| Diseño de interfaz | Figma, Adobe XD |
| Documentación | Swagger / OpenAPI, Javadoc, Doxygen |

**Herramientas históricas:** *Rational Rose* fue la referencia en modelado UML durante los años 90
y 2000, pero está discontinuada. Su lugar lo ocuparon Enterprise Architect y StarUML.

---

### La IA generativa como herramienta CASE
<!-- .slide: style="font-size: 0.75em" -->

Es la categoría más nueva y, en volumen de uso, ya la más extendida.

Según la investigación de JetBrains de 2026, **el 90% de los desarrolladores profesionales usa
agentes de IA para programar al menos una vez por semana**, y el 68% lo hace a diario. El 70% usa
entre dos y cuatro de estas herramientas en paralelo.

**Ejemplos:** GitHub Copilot, Claude Code, Cursor, Codex.

Responden exactamente a la definición de CASE que vimos al principio: **automatizan actividades del
proceso y brindan información sobre el software que se desarrolla.** La diferencia es en qué
actividades.

----

### ¿Dónde encaja en la clasificación?
<!-- .slide: style="font-size: 0.72em" -->

| Función de la clasificación | Qué hace un asistente de IA |
|---|---|
| Análisis y diseño | Redacta y critica requerimientos, propone modelos |
| Programación | Genera y completa código, explica código ajeno |
| Integración y prueba | Escribe casos de prueba, detecta defectos |
| Mantenimiento | Refactoriza, documenta código heredado, hace ingeniería inversa |
| Soporte | Genera documentación técnica |

**El problema:** cruza casi todas las categorías a la vez. La taxonomía Upper/Lower CASE fue
pensada cuando cada herramienta hacía una cosa; una herramienta que atraviesa todo el ciclo de vida
es, por definición, **I-CASE**, pero no se parece en nada a los I-CASE de los años 90.

----

### Límites y riesgos
<!-- .slide: style="font-size: 0.78em" -->

Se aplican las mismas desventajas que ya vimos, más algunas propias:

- **Genera código plausible, no necesariamente correcto.** La verificación sigue siendo humana.
- **Dependencia**: un equipo que no entiende el código que acepta no puede mantenerlo.
- **Confidencialidad**: enviar código propietario a un servicio externo puede violar políticas de
  la organización o contratos con el cliente.
- **Consistencia**: no garantiza que dos soluciones generadas sigan el mismo criterio de diseño.

**No reemplaza al criterio de ingeniería.** Es la razón por la que esta materia sigue existiendo.

----

### 💡 Ejercicio: La IA rompe la taxonomía
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

1. Ubiquen un asistente de IA en las tres clasificaciones vistas: ¿Upper o Lower CASE?
   ¿Toolkit, workbench o entorno integrado? ¿Qué función de las ocho?
2. Si la respuesta a alguna de las tres es "depende" o "todas", ¿qué dice eso sobre la
   clasificación?
3. ¿Qué **desventaja** de las que vimos se agrava con estas herramientas y cuál se atenúa?

<!--
1. No entra limpio en ninguna: cubre desde requerimientos hasta mantenimiento (I-CASE por
   cobertura), pero su integración depende de dónde esté embebido (dentro del IDE es workbench;
   como agente autónomo se parece más a un entorno integrado).
2. Que las taxonomías son herederas de su época. Clasificaban productos que hacían una cosa.
   No es que la clasificación esté "mal": describe bien un panorama que cambió.
3. Se agrava la dependencia y la funcionalidad limitada (el equipo pierde comprensión del código,
   y la herramienta no conoce las reglas de negocio específicas). Se atenúan el costo de
   adquisición y la curva de aprendizaje: hoy la barrera de entrada es casi nula.
-->

<!--https://quinterod.wordpress.com/wp-content/uploads/2015/09/herramientas-case.pdf-->
<!--https://repositorio.utn.edu.ec/bitstream/123456789/1087/2/04%20ISC%20001-TESIS.pdf-->
<!--https://marcochicaiza72.blogspot.com/p/herramientas-case.html-->

---

### 💡 Ejercicio: Ubicar una herramienta
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.72em" -->

Para cada herramienta, indiquen **las tres cosas a la vez**: qué parte del ciclo de vida cubre
(Upper / Lower / I-CASE), qué grado de integración tiene (toolkit / workbench / entorno integrado)
y qué función cumple de las ocho vistas.

| Herramienta | Ciclo de vida | Integración | Función |
|---|---|---|---|
| draw.io | | | |
| Visual Studio Code | | | |
| StarUML | | | |
| Postman | | | |
| GitHub | | | |
| Jira | | | |

<!--
draw.io: Upper - toolkit - análisis y diseño.
VS Code: Lower - workbench (editor + depurador + terminal + extensiones) - programación.
StarUML: Upper - workbench (modela y genera código) - análisis y diseño.
Postman: Lower - toolkit - integración y prueba.
GitHub: transversal, se acerca a I-CASE - entorno integrado - soporte + gestión de proyectos.
Jira: transversal - toolkit - gestión de proyectos.
El punto del ejercicio: las tres clasificaciones son puntos de vista distintos sobre la misma
herramienta, no cajones donde entra en uno solo.
-->

---

### 💡 Ejercicio: Armar el entorno de un proyecto
<!-- .slide: class="exercise-slide" -->
<!-- .slide: style="font-size: 0.75em" -->

Son un equipo de **4 personas** que debe construir el sistema de turnos de un centro médico en
**cuatro meses**, con **presupuesto cero** para licencias.

1. Elijan las herramientas que usarían y ubiquen cada una en la función que cubre.
2. ¿Qué fase del ciclo de vida les queda **sin herramienta**? ¿Es un problema?
3. Justifiquen **una** herramienta que decidieron *no* usar aunque exista.

<!--
Lo que interesa evaluar:
- Que cubran modelado, desarrollo, versionado, pruebas y gestión, no solo el IDE.
- Que noten que presupuesto cero no es una limitación real hoy: casi todo el stack profesional
  tiene alternativa libre o gratuita (VS Code, Git, GitHub, draw.io, StarUML, Postman, Jira free).
- El punto 3 es el más formativo: descartar una herramienta por sobrecarga de proceso es una
  decisión de ingeniería tan válida como adoptarla.
-->

---

### De "CASE" a "toolchain"
<!-- .slide: style="font-size: 0.75em" -->

**Un aviso antes de terminar:** en un equipo de desarrollo nadie dice "voy a usar una herramienta
CASE". El término es de la bibliografía académica y los años 80, y hoy está prácticamente en desuso
en la industria.

| Lo que dice la bibliografía | Lo que van a escuchar en un trabajo |
|---|---|
| Herramientas CASE | Herramientas, *tooling* |
| Conjunto de herramientas CASE integradas | *Toolchain*, *stack* |
| IPSE | Plataforma de desarrollo (GitHub, GitLab, Azure DevOps) |
| Herramientas de integración y prueba | CI/CD |
| Herramientas de mantenimiento | Observabilidad, calidad de código |
| Repositorio | Control de versiones, monorepo |

**El concepto no cambió, cambió el nombre.** Vale la pena conocer los dos: uno entra en el examen
y en la bibliografía, el otro se usa todos los días.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
