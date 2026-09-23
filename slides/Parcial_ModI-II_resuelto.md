---
title: Parcial resuelto - Módulos I y II
theme: solarized
slideNumber: true
---

#### Ingeniería de Software
# Parcial resuelto
### Módulos I y II · Tema A

---
<!-- .slide: style="font-size: 0.80em" -->
<style>
.grid-item {
    border: 3px solid rgba(121, 177, 217, 0.8);
    padding: 20px;
    text-align: left !important;
}

.fuente {
  border-top: 2px solid rgba(121, 177, 217, 0.6);
  padding-top: 10px;
  margin-top: 18px;
  font-size: 0.72em;
}

.fuente a { text-decoration: none; }
</style>

## Cómo usar este repaso

Cada ítem del parcial está resuelto y, al pie, tiene los **enlaces a las filminas exactas**
donde se desarrolla el tema.

<div class="grid-item">

Los enlaces abren la filmina **en la diapositiva precisa**, no al principio del mazo.
Si una respuesta no te cierra, entrá por ahí antes de preguntar.

</div>

**Ojo:** las respuestas son orientativas. En los ítems de desarrollo se evalúa la
**justificación**, no que coincidan palabra por palabra con esto.

---

## Ítem 1
### Los cuatro atributos esenciales

<!-- .slide: style="font-size: 0.68em" -->

* **Mantenimiento** — el software debe poder evolucionar para satisfacer las necesidades
  cambiantes de los clientes.
* **Confiabilidad y seguridad** — funcionar sin fallos graves, y que usuarios
  malintencionados no puedan acceder al sistema ni dañarlo.
* **Eficiencia** — optimizar el uso de memoria, procesador y tiempo de respuesta.
* **Aceptabilidad** — ser comprensible, utilizable y compatible para el usuario al que
  está destinado.

<div class="fuente">

📎 [Atributos esenciales — definición](U1_Introduccion.html#/20/0) ·
[los cuatro, en detalle](U1_Introduccion.html#/20/1) ·
[continuación](U1_Introduccion.html#/20/2)

</div>
 
---

## Ítem 2
### Las cinco fases del modelo de cascada

<!-- .slide: style="font-size: 0.72em" -->

1. Análisis y definición de requerimientos
2. Diseño del sistema y del software
3. Implementación y prueba de unidades
4. Integración y prueba del sistema
5. Operación y mantenimiento

En principio, **una fase debe completarse antes de pasar a la siguiente**. De ahí su principal
inconveniente: la dificultad para acomodar cambios una vez iniciado el proceso.

<div class="fuente">

📎 [Modelo de Cascada](U2_procesos_software.html#/7/0) ·
[Fases del modelo](U2_procesos_software.html#/7/1) ·
[Problemas del modelo](U2_procesos_software.html#/7/2) ·
[Cascada en la práctica](U2_procesos_software.html#/7/3)

</div>

----

## Ítem 2
### ¿Qué cambia entre cascada e incremental?

<!-- .slide: style="font-size: 0.75em" -->

**No cambia *qué* se hace, sino *cuándo* y *cuántas veces*.**

Las cuatro actividades fundamentales —especificación, diseño e implementación, validación y
evolución— están en los dos modelos.

* En **cascada** se organizan en **secuencia** y se recorren **una sola vez**.
* En **incremental** se **intercalan** y se **repiten en cada incremento**.

Lo que define a un modelo de proceso es el **ordenamiento** de las actividades, no las
actividades en sí.

<div class="fuente">

📎 [Las cuatro actividades](U2_procesos_software.html#/17/0) ·
[Cómo se ordenan según el modelo](U2_procesos_software.html#/18/0) ·
[Los modelos de proceso](U2_procesos_software.html#/5/0)

</div>

---

## Ítem 3
### Dirigido por plan vs. Ágil

<!-- .slide: style="font-size: 0.62em" -->

| Criterio | Dirigido por plan | Ágil |
|---|---|---|
| **Incertidumbre que tolera** | Baja: los requisitos son estables y se conocen desde el inicio | Alta: se espera que cambien durante el proyecto |
| **Cumplir normativas** | Crítica: exige trazabilidad y documentación auditable | No obligatoria; con normativa estricta el enfoque puro deja de servir |
| **Tamaño del equipo** | Grande y estructurado, incluso distribuido en varias sedes | Pequeño y flexible, con comunicación informal |
| **Ejemplo de proyecto** | Aviónica, dispositivo médico, backend bancario | App de una startup, e-commerce, app de consumo |

<div class="fuente">

📎 [Plan vs. ágil](U2_procesos_software.html#/4/0) ·
[Cuadro comparativo completo](U2_procesos_software.html#/9/5) ·
[Ejercicio de escenarios](U2_procesos_software.html#/9/0) ·
[Desarrollo guiado por plan y ágil](U4_1_desarrollo_agil.html#/13/0)

</div>

---

## Ítem 4
### Scrum: roles, artefactos y ceremonias

<!-- .slide: style="font-size: 0.70em" -->

* **Roles:** Product Owner · Scrum Master · Equipo de Desarrollo
  *(el material suma también el rol de UX)*
* **Artefactos:** Product Backlog · Sprint Backlog · Incremento
* **Ceremonias:** Sprint Planning · Daily Meeting · Sprint Review o Demo · Retrospectiva ·
  Refinamiento o Grooming

<div class="fuente">

📎 [Roles](U4P_scrum_jira.html#/4/0) ·
[Artefactos](U4P_scrum_jira.html#/5/0) ·
[Ceremonias](U4P_scrum_jira.html#/7/0)

</div>

----

## Ítem 4
### Quién ordena y quién estima

<!-- .slide: style="font-size: 0.72em" -->

El **Product Owner** ordena y prioriza el Product Backlog: es el único perfil que habla
constantemente con el cliente y conoce el valor de negocio de cada tarea.

El **Equipo de Desarrollo** estima, y es el único que lo hace, **sin dejarse influenciar por
nadie**.

**¿Por qué no la misma persona?** Para que quien quiere que algo se haga rápido no sea el
mismo que decide cuánto cuesta. Separar la priorización de la estimación evita que la presión
por entregar distorsione los tiempos, y hace que el compromiso del sprint sea **realista en
lugar de impuesto**.

<div class="fuente">

📎 [Rol: Product Owner](U4P_scrum_jira.html#/4/1) ·
[Rol: Equipo de desarrollo](U4P_scrum_jira.html#/4/3) ·
[Product Backlog](U4P_scrum_jira.html#/6/0) ·
[Sprint Planning](U4P_scrum_jira.html#/7/1)

</div>

---

## Ítem 5
### Herramientas CASE por cobertura del ciclo de vida

<!-- .slide: style="font-size: 0.62em" -->

| Categoría | ¿Qué fases cubre? | Una herramienta |
|---|---|---|
| **Upper CASE** | Fases iniciales: planificación, análisis y diseño. Trabaja con modelos y diagramas, lejos del código | StarUML, Lucidchart, draw.io |
| **Lower CASE** | Fases finales: implementación, pruebas y mantenimiento. Trabaja sobre el código | VS Code, JUnit, Postman |
| **I-CASE** | Todo el ciclo de vida de forma integrada, conectando los modelos del análisis con el código | GitHub, GitLab |

**Las otras dos clasificaciones:** por **grado de integración** (toolkit, workbench, entorno
integrado) y por **función** (ocho categorías). No son alternativas: una misma herramienta se
ubica en las tres a la vez.

<div class="fuente">

📎 [Las tres clasificaciones](U2_herramientas-case.html#/12/0) ·
[Por cobertura del ciclo de vida](U2_herramientas-case.html#/13/0) ·
[Por grado de integración](U2_herramientas-case.html#/14/0) ·
[Por función](U2_herramientas-case.html#/15/0) ·
[Herramientas en uso hoy](U2_herramientas-case.html#/17/0)

</div>

---

## Ítem 6
### Clasificación de requerimientos

<!-- .slide: style="font-size: 0.62em" -->

| # | Requerimiento | Clasificación |
|---|---|---|
| a | Procesar 500 transacciones por segundo | **No funcional** — producto (rendimiento) |
| b | Enviar un correo al registrarse un pedido | **Funcional** |
| c | Cumplir la Ley 25.326 de Datos Personales | **No funcional** — externo (legal) |
| d | El backend debe desarrollarse en Java | **No funcional** — organizacional |
| e | Asignar un identificador único a cada orden | **Funcional** |
| f | Aprendizaje menor a 30 minutos | **No funcional** — producto (usabilidad) |

Un no funcional puede ser **más crítico** que uno funcional: si no se cumple, el sistema
resulta inutilizable aunque todas sus funciones estén implementadas.

<div class="fuente">

📎 [Funcionales y no funcionales](U3_ingenieria_requerimientos.html#/10/0) ·
[Clasificación de los no funcionales](U3_ingenieria_requerimientos.html#/16/0) ·
[Tipos de no funcionales](U3_ingenieria_requerimientos.html#/17/0) ·
[Ejercicio de clasificación](U3_ingenieria_requerimientos.html#/27/0)

</div>

---

## Ítem 7
### Qué va en cada sección del SRS

<!-- .slide: style="font-size: 0.60em" -->

| Sección | ¿Qué se documenta ahí? |
|---|---|
| **Alcance** | Los límites del producto: qué funcionalidades incluye, cuáles quedan explícitamente excluidas, beneficios y objetivos medibles |
| **Restricciones** | Limitaciones a las que está sujeto el desarrollo: normativa, hardware, protocolos, seguridad, plazos, tecnologías impuestas |
| **Supuestos y dependencias** | Lo que se da por cierto y que, de ser falso, invalidaría requerimientos; y los factores externos fuera del control del equipo |
| **Requerimientos específicos** | Todos los requerimientos con detalle suficiente para diseñar el sistema y para que los testers deriven los casos de prueba |

<div class="fuente">

📎 [Alcance](U3P_requerimientos_de_software.html#/6/0) ·
[Alcance: cómo se ve](U3P_requerimientos_de_software.html#/6/1) ·
[Restricciones](U3P_requerimientos_de_software.html#/15/0) ·
[Supuestos y dependencias](U3P_requerimientos_de_software.html#/16/0) ·
[Requerimientos específicos](U3P_requerimientos_de_software.html#/18/0)

</div>

---

## Ítem 8
### Redactar el requerimiento completo

<!-- .slide: style="font-size: 0.58em" -->

**RF-07 — Cancelación de turno por el paciente**

* **Descripción:** el sistema deberá permitir que un paciente cancele un turno propio a través
  de la web.
* **Entradas:** identificador del turno e identificador del paciente autenticado.
* **Precondición:** el turno existe, está en estado *Confirmado* y faltan más de 24 horas para
  su inicio.
* **Proceso:** verifica la precondición, cambia el estado a *Cancelado*, libera la franja en la
  agenda del profesional y registra la operación en la bitácora.
* **Salidas:** confirmación en pantalla y correo de aviso al paciente.
* **Postcondición:** la franja queda disponible para otro paciente.
* **Excepción:** si faltan menos de 24 horas, se rechaza y se indica comunicarse con recepción.

De la **precondición** y la **excepción** salen dos casos de prueba casi sin pensar. Ese es el
estándar al que hay que llegar.

<div class="fuente">

📎 [Cómo se escribe uno, en concreto](U3P_requerimientos_de_software.html#/20/1) ·
[Requerimientos funcionales](U3P_requerimientos_de_software.html#/20/0) ·
[Requerimientos específicos](U3P_requerimientos_de_software.html#/18/0)

</div>

---

## Ítem 9
### Técnicas de prototipado por fidelidad

<!-- .slide: style="font-size: 0.60em" -->

| Técnica | Fidelidad | Entregable | ¿Qué pregunta responde? |
|---|---|---|---|
| **Sketch** | Muy baja | Dibujo a mano, en papel | ¿Vale la pena esta idea? Explorar y descartar sin costo |
| **Wireframe** | Baja | Imagen estática | ¿Está toda la información y bien jerarquizada? |
| **Mockup** | Media / alta | Imagen estática | ¿Se ve como queremos? Aspecto visual final |
| **Prototipo** | Media / alta | Archivo navegable (HTML, Figma) | ¿La gente puede usarlo? Interacción real |

Lo que separa al **mockup** del **prototipo** no es el detalle del dibujo: es la
**navegabilidad**. Un mockup muy detallado sigue siendo una imagen.

<div class="fuente">

📎 [Las técnicas ordenadas por fidelidad](U4P_prototipado.html#/4/0) ·
[Sketch](U4P_prototipado.html#/6/0) ·
[Wireframe](U4P_prototipado.html#/10/0) ·
[Mockup](U4P_prototipado.html#/14/0) ·
[Prototipo](U4P_prototipado.html#/16/0) ·
[Tabla comparativa](U4P_prototipado.html#/19/1)

</div>

---

## Las tres ideas que atraviesan el parcial

<!-- .slide: style="font-size: 0.80em" -->

1. **Lo que cambia entre modelos de proceso no es qué se hace, sino cuándo y cuántas veces.**
2. **Todo modelo y toda herramienta optimizan algo y pagan con otra cosa.** No hay uno mejor:
   hay uno más adecuado a un contexto, y esa elección se justifica.
3. **Un requerimiento que no se puede verificar todavía no está terminado.** Vale igual para
   los funcionales, los no funcionales y los objetivos de usabilidad.

---
## ¿Dudas, Preguntas, Comentarios?
![DUDAS](images/pregunta.gif)
